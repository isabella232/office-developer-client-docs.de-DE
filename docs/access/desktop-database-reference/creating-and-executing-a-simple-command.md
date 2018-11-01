---
title: Erstellen und Ausführen eines einfachen Befehls
TOCTitle: Creating and Executing a Simple Command
ms:assetid: 9ace1abe-cfae-0677-bc57-5cbda85b79db
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249699(v=office.15)
ms:contentKeyID: 48546547
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0446654a6ad39246289690c95f160bd77dcde19d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886263"
---
# <a name="creating-and-executing-a-simple-command"></a><span data-ttu-id="71e39-102">Erstellen und Ausführen eines einfachen Befehls</span><span class="sxs-lookup"><span data-stu-id="71e39-102">Creating and Executing a Simple Command</span></span>


<span data-ttu-id="71e39-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="71e39-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="71e39-p101">Der folgende Code ist zwar nicht typisch für das **Command** -Objekt, veranschaulicht aber die grundlegende Verwendungsweise des **Command** -Objekts, um einen Befehl für eine Datenquelle auszuführen. In diesem Fall handelt es sich um einen Befehl zum Zurückgeben von Zeilen, mit dem das Ergebnis der Befehlsausführung in einem **Recordset** -Objekt ausgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="71e39-p101">Though not a typical usage of the **Command** object, the following code shows the basic method of using the **Command** object to execute a command against a data source. In this case, it is a row-returning command, so it returns the results of the command execution into a **Recordset** object.</span></span>

```vb 
 
 'BeginBasicCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objRs As New ADODB.Recordset 
 
 objCmd.CommandText = "SELECT OrderID, OrderDate, " & _ 
 "RequiredDate, ShippedDate " & _ 
 "FROM Orders " & _ 
 "WHERE CustomerID = 'ALFKI' " & _ 
 "ORDER BY OrderID" 
 objCmd.CommandType = adCmdText 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 objCmd.ActiveConnection = objConn 
 
 ' Execute once and display... 
 Set objRs = objCmd.Execute 
 
 Debug.Print "ALFKI" 
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
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
'EndBasicCmd 
```

<span data-ttu-id="71e39-106">Der auszuführende Befehl wird mit der **CommandText** -Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="71e39-106">The command to be executed is specified with the **CommandText** property.</span></span>


> [!NOTE]
> <span data-ttu-id="71e39-107">Einige Beispiele in diesem Abschnitt rufen Sie eine Hilfsfunktion **GetNewConnection**herstellen eine Verbindung mit dem Datenanbieter.</span><span class="sxs-lookup"><span data-stu-id="71e39-107">Several examples in this section call a utility function, **GetNewConnection**, to establish a connection with the data provider.</span></span> <span data-ttu-id="71e39-108">Um Redundanz zu vermeiden, wird sie nur einmal aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="71e39-108">To avoid redundancy, it is listed only once:</span></span>

```vb 
 
'BeginNewConnection 
Private Function GetNewConnection() As ADODB.Connection 
 Dim oCn As New ADODB.Connection 
 Dim sCnStr As String 
 
 sCnStr = "Provider='SQLOLEDB';Data Source='MySqlServer';" & _ 
 "Integrated Security='SSPI';Database='Northwind';" 
 oCn.Open sCnStr 
 
 If oCn.State = adStateOpen Then 
 Set GetNewConnection = oCn 
 End If 
 
End Function 
'EndNewConnection 
```

