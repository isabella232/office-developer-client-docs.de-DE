---
title: BeginTrans-, CommitTrans-, RollbackTrans-Methode (Beispiel) (VB)
TOCTitle: BeginTrans, CommitTrans, and RollbackTrans methods example (VB)
ms:assetid: 12fce322-dba7-9159-8a09-7f6daf1a80ed
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248904(v=office.15)
ms:contentKeyID: 48543357
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: a904c56275a66c4ba53b1b9c21e39a0f8ea6a1e5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607115"
---
# <a name="begintrans-committrans-and-rollbacktrans-methods-example-vb"></a>BeginTrans-, CommitTrans- und RollbackTrans-Methode (Beispiel) (VB)


**Gilt für**: Access 2013, Office 2013

In diesem Beispiel wird der Buchtyp aller Bücher in der Tabelle ***Titel** _ der Datenbank geändert. Nachdem die [BeginTrans-Methode](begintrans-committrans-and-rollbacktrans-methods-ado.md) eine Transaktion gestartet hat, die alle an der Tabelle *__Titles_** vorgenommenen Änderungen isoliert, speichert die [CommitTrans-Methode](begintrans-committrans-and-rollbacktrans-methods-ado.md) die Änderungen. Sie können die [RollbackTrans](begintrans-committrans-and-rollbacktrans-methods-ado.md)-Methode verwenden, um mit der [Update](update-method-ado.md)-Methode gespeicherte Änderungen rückgängig zu machen.

```vb 
 
'BeginBeginTransVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim strCnxn As String 
 Dim rstTitles As ADODB.Recordset 
 Dim strSQLTitles As String 
 'record variables 
 Dim strTitle As String 
 Dim strMessage As String 
 
 ' Open connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' Open recordset dynamic to allow for changes 
 Set rstTitles = New ADODB.Recordset 
 strSQLTitles = "Titles" 
 rstTitles.Open strSQLTitles, Cnxn, adOpenDynamic, adLockPessimistic, adCmdTable 
 
 Cnxn.BeginTrans 
 
 ' Loop through recordset and prompt user 
 ' to change the type for a specified title 
 
 rstTitles.MoveFirst 
 
 Do Until rstTitles.EOF 
 If Trim(rstTitles!Type) = "psychology" Then 
 strTitle = rstTitles!Title 
 strMessage = "Title: " & strTitle & vbCr & _ 
 "Change type to self help?" 
 
 ' If yes, change type for the specified title 
 If MsgBox(strMessage, vbYesNo) = vbYes Then 
 rstTitles!Type = "self_help" 
 rstTitles.Update 
 End If 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' Prompt user to commit all changes made 
 If MsgBox("Save all changes?", vbYesNo) = vbYes Then 
 Cnxn.CommitTrans 
 Else 
 Cnxn.RollbackTrans 
 End If 
 
 ' Print recordset 
 rstTitles.Requery 
 rstTitles.MoveFirst 
 Do While Not rstTitles.EOF 
 Debug.Print rstTitles!Title & " - " & rstTitles!Type 
 rstTitles.MoveNext 
 Loop 
 
 ' Restore original data as this is a demo 
 rstTitles.MoveFirst 
 
 Do Until rstTitles.EOF 
 If Trim(rstTitles!Type) = "self_help" Then 
 rstTitles!Type = "psychology" 
 rstTitles.Update 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' clean up 
 rstTitles.Close 
 Cnxn.Close 
 Set rstTitles = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstTitles Is Nothing Then 
 If rstTitles.State = adStateOpen Then rstTitles.Close 
 End If 
 Set rstTitles = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
 
 
'EndBeginTransVB 
```

