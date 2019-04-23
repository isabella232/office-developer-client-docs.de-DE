---
title: Benannte Befehle
TOCTitle: Named commands
ms:assetid: 1a4d77e0-1736-83ea-a3c6-f5398c0b01e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248948(v=office.15)
ms:contentKeyID: 48543518
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 40ce95c5879f5da9615c66d132d6c4847fae1569
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288644"
---
# <a name="named-commands"></a><span data-ttu-id="97bb8-102">Benannte Befehle</span><span class="sxs-lookup"><span data-stu-id="97bb8-102">Named commands</span></span>


<span data-ttu-id="97bb8-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97bb8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="97bb8-104">Sie können die **Name** -Eigenschaft für ein **Command** -Objekt festlegen und dann den Befehl ausführen, indem Sie ihn aufrufen, als wäre es eine Methode für die **ActiveConnection** -Eigenschaft des **Command** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="97bb8-104">You can set the **Name** property on a **Command** object and then execute the command by calling it as if it were a method on the **Command** object **ActiveConnection** property.</span></span> <span data-ttu-id="97bb8-105">Dies wird im folgenden Beispiel veranschaulicht, in dem der Befehl getCustomers \*\* heißt.</span><span class="sxs-lookup"><span data-stu-id="97bb8-105">This is illustrated in the following example, in which the command is named *GetCustomers*.</span></span> <span data-ttu-id="97bb8-106">Beachten Sie, dass der Code ein deklariertes und instanziiertes **Recordset** -Objekt an die GetCustomers-Methode übergibt.</span><span class="sxs-lookup"><span data-stu-id="97bb8-106">Notice that the code passes in a declared and instantiated **Recordset** object to the GetCustomers "method."</span></span> <span data-ttu-id="97bb8-107">Sie können auch Parameter an die "Method" übergeben, wenn Sie für den **Befehl**erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="97bb8-107">You can also pass in parameters to the "method" if they are required by the **Command**.</span></span>

```vb 
 
'BeginNamedCmd 
 On Error GoTo ErrHandler: 
 
 Dim objConn As New ADODB.Connection 
 Dim objCmd As New ADODB.Command 
 Dim objRs As New ADODB.Recordset 
 
 ' Connect to the data source. 
 Set objConn = GetNewConnection 
 
 objCmd.CommandText = "SELECT CustomerID, CompanyName FROM Customers" 
 objCmd.CommandType = adCmdText 
 
 'Name the command. 
 objCmd.Name = "GetCustomers" 
 
 objCmd.ActiveConnection = objConn 
 
 ' Execute using Command.Name from the Connection. 
 objConn.GetCustomers objRs 
 
 ' Display. 
 Do While Not objRs.EOF 
 Debug.Print objRs(0) & vbTab & objRs(1) 
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
'EndNamedCmd 
```

