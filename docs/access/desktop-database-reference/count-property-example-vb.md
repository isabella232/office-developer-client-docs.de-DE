---
title: Count-Eigenschaft (Beispiel) (VB)
TOCTitle: Count property example (VB)
ms:assetid: 9fea66f7-a4ed-fe2e-c199-672b910fef47
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249734(v=office.15)
ms:contentKeyID: 48546695
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 675dd1f671bd70d8272e303708bf951bbcee1a47
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295464"
---
# <a name="count-property-example-vb"></a><span data-ttu-id="fe276-102">Count-Eigenschaft (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="fe276-102">Count property example (VB)</span></span>


<span data-ttu-id="fe276-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="fe276-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fe276-104">In diesem Beispiel wird die [count](count-property-ado.md) -Eigenschaft mit zwei Auflistungen in der ***Employee*** -Datenbank veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fe276-104">This example demonstrates the [Count](count-property-ado.md) property with two collections in the ***Employee*** database.</span></span> <span data-ttu-id="fe276-105">Die-Eigenschaft ruft die Anzahl der Objekte in jeder Auflistung ab und legt die obere Grenze für Schleifen fest, die diese Auflistungen auflisten.</span><span class="sxs-lookup"><span data-stu-id="fe276-105">The property obtains the number of objects in each collection, and sets the upper limit for loops that enumerate these collections.</span></span> <span data-ttu-id="fe276-106">Eine andere Möglichkeit zum Aufzählen dieser Auflistungen ohne Verwendung der **count** -Eigenschaft wäre das Verwenden von Anweisungen.</span><span class="sxs-lookup"><span data-stu-id="fe276-106">Another way to enumerate these collections without using the **Count** property would be to use statements.</span></span>

```vb 
 
'BeginCountVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' recordset and connection variables 
 Dim rstEmployees As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim strSQLEmployees As String 
 Dim strCnxn As String 
 
 Dim intLoop As Integer 
 
 ' Open a connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Northwind';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset with data from Employee table 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployees = "Employees" 
 'rstEmployees.Open strSQLEmployee, Cnxn, , , adCmdTable 
 rstEmployees.Open strSQLEmployees, Cnxn, adOpenForwardOnly, adLockReadOnly, adCmdTable 
 'the above two lines opening the recordset are identical as 
 'the default values for CursorType and LockType arguments match those specified 
 
 ' Print information about Fields collection 
 Debug.Print rstEmployees.Fields.Count & " Fields in Employee" 
 
 For intLoop = 0 To rstEmployees.Fields.Count - 1 
 Debug.Print " " & rstEmployees.Fields(intLoop).Name 
 Next intLoop 
 
 ' Print information about Properties collection 
 Debug.Print rstEmployees.Properties.Count & " Properties in Employee" 
 
 For intLoop = 0 To rstEmployees.Properties.Count - 1 
 Debug.Print " " & rstEmployees.Properties(intLoop).Name 
 Next intLoop 
 
 ' clean up 
 rstEmployees.Close 
 Cnxn.Close 
 Set rstEmployees = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndCountVB 
```

