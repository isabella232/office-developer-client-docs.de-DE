---
title: Aufrufen einer gespeicherten Prozedur mithilfe eines Befehls
TOCTitle: Calling a Stored Procedure with a Command
ms:assetid: 19d600d7-f717-39df-11a0-951e3ed0f812
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248944(v=office.15)
ms:contentKeyID: 48543509
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 573b847f53d3fc7ca07691e9a92d152598531bce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25474328"
---
# <a name="calling-a-stored-procedure-with-a-command"></a>Aufrufen einer gespeicherten Prozedur mithilfe eines Befehls


**Betrifft**: Access 2013 | Office 2013

Zum Aufrufen einer gespeicherten Prozedur können Sie auch einen Befehl verwenden. Mit dem folgenden Code wird in der Northwind-Beispiedatenbank die gespeicherte Prozedur CustOrdersOrders aufgerufen, die wie folgt definiert ist:

```vb 
 
CREATE PROCEDURE CustOrdersOrders @CustomerID nchar(5) AS 
SELECT OrderID, OrderDate, RequiredDate, ShippedDate 
FROM Orders 
WHERE CustomerID = @CustomerID 
ORDER BY OrderID 
```

Diese gespeicherte Prozedur ähnelt dem in [Parameter des Command-Objekts](command-object-parameters.md) verwendeten Befehl, insofern als anhand eines Parameters für die Kunden-Nr. Informationen zu den Bestellungen dieses Kunden zurückgegeben werden. Im folgenden Code wird diese gespeicherte Prozedur als Quelle für ein **Recordset** -ADO-Objekt verwendet.

Mithilfe der gespeicherten Prozedur haben Sie Zugriff auf eine andere ADO-Funktion, nämlich die **Refresh** -Methode der **Parameters** -Auflistung. Mit dieser Methode kann ADO zur Laufzeit automatisch alle Informationen zu den für den Befehl erforderlichen Parametern eingeben. Durch diese Technik wird die Leistung beeinträchtigt, da ADO die Informationen zu den Parametern von der Datenquelle abfragen muss.

Es gibt weitere wichtige Unterschiede zwischen dem folgenden Code und dem Code in [Parameter des Command-Objekts](command-object-parameters.md), bei dem die Parameter manuell eingegeben wurden. Erstens wird mit diesem Code die **Prepared** -Eigenschaft nicht auf **True** festgelegt, weil es sich um eine gespeicherte SQL Server-Prozedur handelt und sie gemäß Definition vorkompiliert ist. Zweitens wurde die **CommandType** -Eigenschaft des **Command** -Objekts im zweiten Beispiel in **adCmdStoredProc** geändert, um ADO zu informieren, dass es sich bei dem Befehl um eine gespeicherte Prozedur handelt.

```vb 
 
'BeginAutoParamCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objParm1 As New ADODB.Parameter 
 Dim objRs As New ADODB.Recordset 
 
 ' Set CommandText equal to the stored procedure name. 
 objCmd.CommandText = "CustOrdersOrders" 
 objCmd.CommandType = adCmdStoredProc 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Automatically fill in parameter info from stored procedure. 
 objCmd.Parameters.Refresh 
 
 ' Set the param value. 
 objCmd(1) = "ALFKI" 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print objParm1.Value 
 Do While Not objRs.EOF 
 Debug.Print vbTab & objRs(0) & vbTab & objRs(1) & vbTab & _ 
 objRs(2) & vbTab & objRs(3) 
 objRs.MoveNext 
 Loop 
 
 ' ...then set new param value, re-execute command, and display. 
 objCmd(1) = "CACTU" 
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
'EndAutoParamCmd 
```

