---
title: Parameter des Command-Objekts
TOCTitle: Command object parameters
ms:assetid: b43bb20e-9d0a-b361-6845-d537ae667f0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249862(v=office.15)
ms:contentKeyID: 48547218
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 0cdced5913f397887f9bc69e2db96e59ee43bfe0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59632112"
---
# <a name="command-object-parameters"></a>Parameter des Command-Objekts

**Gilt für**: Access 2013, Office 2013

Eine interessantere Verwendung für das **Command** -Objekt wird im nächsten Beispiel veranschaulicht, in dem der Text des SQL-Befehls geändert und dadurch parametrisiert wurde. Auf diese Weise kann der Befehl wiederverwendet werden, wobei jedes Mal ein anderer Wert an den Parameter übergeben wird. Die **Prepared** -Eigenschaft im **Command** -Objekt ist auf **True** festgelegt. Deshalb erfordert ADO, dass der Anbieter den in der **CommandText** -Eigenschaft angegebenen Befehl kompiliert, bevor er zum ersten Mal ausgeführt wird. Außerdem bleibt der kompilierte Befehl im Arbeitsspeicher gespeichert. Die erstmalige Ausführung des Befehls ist aufgrund der vorbereitenden Schritte geringfügig langsamer. Bei jeder weiteren Ausführung wird der Befehl jedoch schneller ausgeführt. Befehle sollten deshalb nur vorbereitet werden, wenn sie mehrmals verwendet werden.

```vb 
 
'BeginManualParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set the CommandText as a parameterized SQL query. 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = ? " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Prepare command since we will be executing it more than once. 
 objCmd.Prepared = True 
 
 ' Create new parameter for CustomerID. Initial value is ALFKI. 
 Set objParm1 = objCmd.CreateParameter("CustId", adChar, _ 
 adParamInput, 5, "ALFKI") 
 objCmd.Parameters.Append objParm1 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd("CustId") = "CACTU" 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 'clean up 
 objRs.Close 
 objConn.Close 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Set objParm1 = Nothing 
 Exit Sub 
 
ErrHandler: 
 'clean up 
 If objRs.State = adStateOpen Then 
 objRs.Close 
 End If 
 
 If objConn.State = adStateOpen Then 
 objConn.Close 
 End If 
 
 Set objRs = Nothing 
 Set objConn = Nothing 
 Set objCmd = Nothing 
 Set objParm1 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndManualParamCmd 
```

Nicht alle Anbieter unterstützen vorbereitete Befehle. Falls die Vorbereitung von Befehlen vom Anbieter nicht unterstützt wird, wird möglicherweise ein Fehler zurückgegeben, sobald diese Eigenschaft auf **True** festgelegt wird. Falls kein Fehler zurückgegeben wird, wird die Anforderung zum Vorbereiten des Befehls ignoriert, und die **Prepared** -Eigenschaft wird auf **False** festgelegt.

