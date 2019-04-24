---
title: Erkennen und Lösen von Konflikten
TOCTitle: Detecting and resolving conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ddd7566be2581fe449872eb576bf7f11e5a806fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293924"
---
# <a name="detecting-and-resolving-conflicts"></a>Erkennen und Lösen von Konflikten

**Gilt für**: Access 2013, Office 2013

## <a name="detecting-and-resolving-conflicts"></a>Erkennen und Lösen von Konflikten

Wenn Sie das **Recordset** -Objekt im sofortigen Aktualisierungsmodus verwenden, ist die Wahrscheinlichkeit von Parallelitätsproblemen wesentlich geringer. Wenn die Anwendung andererseits den Batchaktualisierungsmodus verwendet, besteht eine relativ hohe Wahrscheinlichkeit, dass ein Benutzer einen Datensatz ändert, bevor Änderungen eines anderen Benutzers, der denselben Datensatz bearbeitet, gespeichert werden. In diesem Fall sollte der Konflikt von der Anwendung problemlos behoben werden. Möglicherweise möchten Sie, dass die letzte Person, die eine Aktualisierung an den Server sendet, "gewinnt". Oder Sie möchten, dass der letzte Benutzer entscheidet, welche Aktualisierung Vorrang haben soll, indem Sie ihm die Wahl zwischen den miteinander in Konflikt stehenden Werten lassen.

In jedem Fall stellt ADO die Eigenschaften **UnderlyingValue** und **OriginalValue** des **Field** -Objekts für diese Art von Konflikten bereit. Verwenden Sie diese Eigenschaften in Kombination mit der **Resync** -Methode und der **Filter** -Eigenschaft des **Recordset** -Objekts.

## <a name="detecting-errors"></a>Erkennen von Fehlern

Wenn ADO während einer Batchaktualisierung einen Konflikt findet, wird der **Errors**-Auflistung eine Warnung hinzugefügt. Deshalb sollten Sie unmittelbar nach dem Aufrufen von **BatchUpdate** stets auf Fehler überprüfen. Falls Sie Fehler finden, sollten Sie testen, ob ein Konflikt vorliegt. Im ersten Schritt sollten Sie die **Filter**-Eigenschaft im **Recordset**-Objekt auf **adFilterConflictingRecords** festlegen (die **Filter**-Eigenschaft wird im vorherigen Kapitel behandelt). Dadurch werden im **Recordset**-Objekt nur die Datensätze angezeigt, die einen Konflikt verursachen. Falls die **RecordCount**-Eigenschaft nach diesem Schritt gleich Null ist, wissen Sie, dass der Fehler nicht durch einen Konflikt verursacht wurde.

Wenn Sie **BatchUpdate** aufrufen, generieren ADO und der Anbieter SQL-Anweisungen, um Aktualisierungen in der Datenquelle auszuführen. Beachten Sie, dass für bestimmte Datenquellen Einschränkungen bezüglich der Spaltentypen gelten, die in einer WHERE-Klausel verwendet werden können.

Rufen Sie anschließend die **Resync**-Methode für das **Recordset**-Objekt auf, wobei das Argument *AffectRecords* auf **adAffectGroup** sowie das Argument *ResyncValues* auf **adResyncUnderlyingValues** festgelegt sind. Die **Resync**-Methode aktualisiert die Daten im aktuellen **Recordset**-Objekt in der zugrunde liegenden Datenbank. Mithilfe von **adAffectGroup** stellen Sie sicher, dass nur die Datensätze, die mit der aktuellen Filtereinstellung angezeigt werden (also nur die miteinander in Konflikt stehenden Datensätze), erneut mit der Datenbank synchronisiert werden. Dies könnte bei einem umfangreichen **Recordset**-Objekt einen erheblichen Unterschied hinsichtlich der Leistung ausmachen. Wenn Sie beim Aufrufen von **Resync** das Argument *ResyncValues* auf **adResyncUnderlyingValues** festlegen, stellen Sie sicher, dass die **UnderlyingValue**-Eigenschaft den Wert (der den Konflikt verursacht) aus der Datenbank enthält, dass die **Value**-Eigenschaft den vom Benutzer eingegebenen Wert beibehält und dass die **OriginalValue**-Eigenschaft den ursprünglichen Wert für das Feld enthält (der Wert, der vor dem letzten erfolgreichen **UpdateBatch**-Aufruf vorhanden war). Anschließend können Sie mithilfe dieser Werte den Konflikt programmgesteuert lösen oder den Benutzer auffordern, den gewünschten Wert auszuwählen.

Diese Technik wird im folgenden Codebeispiel dargestellt. In diesem Beispiel wird künstlich ein Konflikt erzeugt, indem mithilfe eines separaten **Recordset** -Objekts ein Wert in der zugrunde liegenden Tabelle geändert wird, bevor **UpdateBatch** aufgerufen wird.

```vb 
 
'BeginConflicts 
    On Error GoTo ErrHandler: 
     
    Dim objRs1 As New ADODB.Recordset 
    Dim objRs2 As New ADODB.Recordset 
    Dim strSQL As String 
    Dim strMsg As String 
     
    strSQL = "SELECT * FROM Shippers WHERE ShipperID = 2" 
                  
    'Open Rs and change a value 
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
    objRs1("Phone") = "(111) 555-1111" 
     
    'Introduce a conflict at the db... 
    objRs2.Open strSQL, strConn, adOpenKeyset, adLockOptimistic, adCmdText 
    objRs2("Phone") = "(999) 555-9999" 
    objRs2.Update 
    objRs2.Close 
    Set objRs2 = Nothing 
     
    On Error Resume Next 
    objRs1.UpdateBatch 
     
    If objRs1.ActiveConnection.Errors.Count <> 0 Then 
        Dim intConflicts As Integer 
         
        intConflicts = 0 
         
        objRs1.Filter = adFilterConflictingRecords 
         
        intConflicts = objRs1.RecordCount 
         
        'Resync so we can see the UnderlyingValue and offer user a choice. 
        'This sample only displays all three values and resets to original. 
        objRs1.Resync adAffectGroup, adResyncUnderlyingValues 
         
        If intConflicts > 0 Then 
            strMsg = "A conflict occurred with updates for " & intConflicts & _ 
                     " record(s)." & vbCrLf & "The values will be restored" & _ 
                     " to their original values." & vbCrLf & vbCrLf 
                      
            objRs1.MoveFirst 
            While Not objRs1.EOF 
                strMsg = strMsg & "SHIPPER = " & objRs1("CompanyName") & vbCrLf 
                strMsg = strMsg & "Value = " & objRs1("Phone").Value & vbCrLf 
                strMsg = strMsg & "UnderlyingValue = " & _ 
                                   objRs1("Phone").UnderlyingValue & vbCrLf 
                strMsg = strMsg & "OriginalValue = " & _ 
                                   objRs1("Phone").OriginalValue & vbCrLf 
                strMsg = strMsg & vbCrLf & "Original value has been restored." 
                   
                MsgBox strMsg, vbOKOnly, _ 
                      "Conflict " & objRs1.AbsolutePosition & _ 
                      " of " & intConflicts 
                   
                objRs1("Phone").Value = objRs1("Phone").OriginalValue 
                objRs1.MoveNext 
            Wend 
             
            objRs1.UpdateBatch adAffectGroup 
        Else 
            'Other error occurred. Minimal handling in this example. 
             strMsg = "Errors occurred during the update. " & _ 
                        objRs1.ActiveConnection.Errors(0).Number & " " & _ 
                        objRs1.ActiveConnection.Errors(0).Description 
        End If 
         
        On Error GoTo 0 
    End If 
     
    objRs1.MoveFirst 
     
    'Clean up 
    objRs1.Close 
    Set objRs1 = Nothing 
    Exit Sub 
     
ErrHandler: 
    
    If Not objRs1 Is Nothing Then 
        If objRs1.State = adStateOpen Then objRs1.Close 
        Set objRs1 = Nothing 
    End If 
     
    If Not objRs2 Is Nothing Then 
        If objRs2.State = adStateOpen Then objRs2.Close 
        Set objRs2 = Nothing 
    End If 
     
    If Err <> 0 Then 
        MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
     
'EndConflicts 
```

Mit der **Status** -Eigenschaft des aktuellen **Record** -Objekts oder eines bestimmten **Field** -Objekts können Sie ermitteln, welche Art von Konflikt aufgetreten ist.

Ausführlichere Informationen zur Fehlerbehandlung finden Sie in [Kapitel 6: Fehlerbehandlung](chapter-6-error-handling.md).

