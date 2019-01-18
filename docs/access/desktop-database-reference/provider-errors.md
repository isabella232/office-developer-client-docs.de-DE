---
title: Anbieterfehler (Access PC-Datenbank-Referenz)
TOCTitle: Provider errors
ms:assetid: 9c39d450-6e67-b2fd-aeb5-849e6b65fd54
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249710(v=office.15)
ms:contentKeyID: 48546592
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d175cdaa007a354d12304dceff0352a923de2291
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28717643"
---
# <a name="provider-errors"></a>Anbieterfehler


**Betrifft**: Access 2013, Office 2013 

Wenn ein Anbieterfehler auftritt, wird der Laufzeitfehler -2147467259 zurückgegeben. Wenn dieser Fehler angezeigt wird, überprüfen Sie die **Errors** -Auflistung des aktiven **Connection** -Objekts, die mindestens einen Fehler mit einer Beschreibung enthält.

## <a name="the-ado-errors-collection"></a>Errors-Auflistung von ADO

Ein ADO-Vorgang kann mehrere Anbieterfehler generieren. Deshalb macht ADO mithilfe des **Connection** -Objekts eine Auflistung mit Fehlerobjekten verfügbar. Diese Auflistung enthält keine Objekte, wenn ein Vorgang erfolgreich abgeschlossen wird. Sie enthält mindestens ein **Error** -Objekt, wenn etwas schief gelaufen ist und der Anbieter mindestens einen Fehler ausgelöst hat. Überprüfen Sie die einzelnen Fehlerobjekte, um die genaue Ursache des Fehlers zu bestimmen.

Wenn Sie alle aufgetretenen Fehler behandelt haben, können Sie die Auflistung durch Aufrufen der **Clear** -Methode leeren. Es ist sehr wichtig, dass die **Errors** -Auflistung geleert wird, bevor Sie die Methoden **Resync**, **UpdateBatch** oder **CancelBatch** für ein **Recordset** -Objekt aufrufen, die **Open** -Methode für ein **Connection** -Objekt aufrufen, oder die **Filter** -Eigenschaft für ein **Recordset** -Objekt festlegen. Durch das explizite Leeren der Auflistung haben Sie die Sicherheit, dass in der Auflistung keine **Error** -Objekte von einem vorherigen Vorgang mehr übrig sind.

Bei manchen Vorgängen können Warnungen sowie Fehler generiert werden. Warnungen werden ebenfalls durch **Error** -Objekte in der **Errors** -Auflistung dargestellt. Wenn ein Anbieter der Auflistung eine Warnung hinzufügt, wird kein Laufzeitfehler generiert. Überprüfen Sie die **Count** -Eigenschaft der **Errors** -Auflistung, um festzustellen, ob von einem bestimmten Vorgang eine Warnung erzeugt wurde. Falls ein Wert von mindestens eins vorhanden ist, wurde der Auflistung ein **Error** -Objekt hinzugefügt. Wenn Sie festgestellt haben, dass die **Errors** -Auflistung Fehler oder Warnungen enthält, können Sie die Auflistung durchlaufen und Informationen zu jedem vorhandenen **Error** -Objekt abrufen. Dies wird anhand des folgenden kurzen Visual Basic-Beispiels veranschaulicht:

```vb 
 
' BeginErrorHandlingVB02 
Private Function DeleteCustomer(ByVal CompanyName As String) As Long 
 On Error GoTo DeleteCustomerError 
 
 rst.Find "CompanyName='" & CompanyName & "'" 
 
DeleteCustomerError: 
 
 Dim objError As ADODB.Error 
 Dim strError As String 
 
 If cnn.Errors.Count > 0 Then 
 For Each objError In cnn.Errors 
 strError = strError & "Error #" & objError.Number & _ 
 " " & objError.Description & vbCrLf & _ 
 "NativeError: " & objError.NativeError & vbCrLf & _ 
 "SQLState: " & objError.SQLState & vbCrLf & _ 
 "Reported by: " & objError.Source & vbCrLf & _ 
 "Help file: " & objError.HelpFile & vbCrLf & _ 
 "Help Context ID: " & objError.HelpContext 
 Next 
 MsgBox strError 
 End If 
End Function 
' EndErrorHandlingVB02 
```

Die Fehlerbehandlungsroutine enthält eine **For Each** -Schleife, mit der jedes Objekt in der **Errors** -Auflistung überprüft wird. In diesem Beispiel wird lediglich eine Meldung zur Anzeige erfasst. Bei einem funktionierenden Programm würden Sie Code erstellen, um für jeden Fehler eine entsprechende Aufgabe auszuführen, wie z. B. alle geöffneten Dateien schließen und das Programm auf geordnete Weise herunterfahren.

## <a name="the-error-object"></a>Error-Objekt

Durch das Überprüfen eines **Error** -Objekts können Sie bestimmen, welcher Fehler aufgetreten ist und, was noch wichtiger ist, welche Anwendung oder welches Objekt den Fehler verursachte. Das **Error** -Objekt weist die folgenden Eigenschaften auf:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Eigenschaftenname</p></th>
<th><p>Beschreibung</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Beschreibung</strong></p></td>
<td><p>Beschreibender Text für den aufgetretenen Fehler.</p></td>
</tr>
<tr class="even">
<td><p><strong>HelpContext-und HelpFile</strong></p></td>
<td><p>Das Hilfethema und die Hilfedatei, die eine Beschreibung des aufgetretenen Fehlers enthalten.</p></td>
</tr>
<tr class="odd">
<td><p><strong>NativeError</strong></p></td>
<td><p>Die anbieterspezifische Fehlernummer.</p></td>
</tr>
<tr class="even">
<td><p><strong>Zahl</strong></p></td>
<td><p>Eine Zahl vom Datentyp Long Integer für die Nummer (aufgeführt in ErrorValueEnum) des aufgetretenen Fehlers.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Source</strong></p></td>
<td><p>Gibt den Namen des Objekts oder der Anwendung an, das bzw. die einen Fehler generierte.</p></td>
</tr>
<tr class="even">
<td><p><strong>SQLState</strong></p></td>
<td><p>Ein aus fünf Zeichen bestehender Fehlercode, den der Anbieter während der Verarbeitung einer SQL-Anweisung zurückgibt.</p></td>
</tr>
</tbody>
</table>


Das **Error** -Objekt von ADO ist weitgehend identisch mit dem standardmäßigen **Err** -Objekt von Visual Basic. Dessen Eigenschaften beschreiben den aufgetretenen Fehler. Neben der Fehlernummer erhalten Sie auch zwei zusammengehörige Informationselemente. Die **NativeError** -Eigenschaft enthält eine Fehlernummer speziell für den verwendeten Anbieter. Im vorherigen Beispiel wird der Microsoft OLE DB-Anbieter für SQL Server verwendet, weshalb **NativeError** Fehler speziell für SQL Server enthält. Die **SQLState** -Eigenschaft weist einen aus fünf Zeichen bestehenden Code auf, mit dem ein Fehler in einer SQL-Anweisung beschrieben wird.

## <a name="event-related-errors"></a>Ereignisbezogene Fehler

Das **Error** -Objekt wird auch verwendet, wenn ereignisbezogene Fehler auftreten. Sie können bestimmen, ob im Prozess ein Fehler aufgetreten ist, durch den ein ADO-Ereignis ausgelöst wurde, indem Sie das **Error** -Objekt überprüfen, das als Ereignisparameter übergeben wurde.

Wenn der Vorgang, der ein Ereignis verursachte, erfolgreich abgeschlossen wird, wird der *adStatus*-Parameter des Ereignishandlers auf *adStatusOK* festgelegt. Wenn andernfalls der Vorgang, der das Ereignis auslöste, nicht erfolgreich war, wird der *adStatus*-Parameter auf *adStatusErrorsOccurred* festgelegt. In diesem Fall enthält der *pError*-Parameter ein **Error**-Objekt, das den Fehler beschreibt.

