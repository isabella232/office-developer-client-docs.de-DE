---
title: Type-Eigenschaft (Beispiel) (Field) (VB)
TOCTitle: Type property example (Field) (VB)
ms:assetid: ff9e26a8-898d-ec89-5093-69c66dbb05ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250314(v=office.15)
ms:contentKeyID: 48548966
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 2426b99b17b33afb31f170216169cf29d4fe0a27
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631671"
---
# <a name="type-property-example-field-vb"></a>Type-Eigenschaft (Beispiel) (Field) (VB)


**Gilt für**: Access 2013, Office 2013

In diesem Beispiel wird die [Type](type-property-ado.md) -Eigenschaft veranschaulicht, indem der Name der Konstante angezeigt wird, die dem Wert der [Type -Eigenschaft](type-property-ado.md) aller [Field -Objekte](field-object-ado.md) in ***der*** Employees -Tabelle entspricht. The FieldType function is required for this procedure to run.

```vb 
 
'BeginTypeFieldVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstEmployees As ADODB.Recordset 
 Dim fld As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLEmployee As String 
 Dim FieldType As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset with data from Employees table 
 Set rstEmployees = New ADODB.Recordset 
 strSQLEmployee = "employee" 
 rstEmployees.Open strSQLEmployee, Cnxn, , , adCmdTable 
 'rstEmployees.Open strSQLEmployee, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 ' the above two lines of code are identical 
 
 Debug.Print "Fields in Employees Table:" & vbCr 
 
 ' Enumerate Fields collection of Employees table 
 For Each fld In rstEmployees.Fields 
 ' translate field-type code to text 
 Select Case fld.Type 
 Case adChar 
 FieldType = "adChar" 
 Case adVarChar 
 FieldType = "adVarChar" 
 Case adSmallInt 
 FieldType = "adSmallInt" 
 Case adUnsignedTinyInt 
 FieldType = "adUnsignedTinyInt" 
 Case adDBTimeStamp 
 FieldType = "adDBTimeStamp" 
 End Select 
 ' show results 
 Debug.Print " Name: " & fld.Name & vbCr & _ 
 " Type: " & FieldType & vbCr 
 Next fld 
 
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
 
 Set fld = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndTypeFieldVB 
```

