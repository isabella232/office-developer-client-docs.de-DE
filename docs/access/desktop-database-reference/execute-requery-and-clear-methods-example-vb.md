---
title: Execute-, Requery- und Clear-Methoden (Beispiel) (VB)
TOCTitle: Execute, Requery, and Clear Methods Example (VB)
ms:assetid: 6d700971-6b77-bd41-dd22-df53f902c0f2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249432(v=office.15)
ms:contentKeyID: 48545491
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6d32d4e0c56ea4b6a03474562410255bbc5952f4
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475017"
---
# <a name="execute-requery-and-clear-methods-example-vb"></a>Execute-, Requery- und Clear-Methoden (Beispiel) (VB)


**Betrifft**: Access 2013 | Office 2013

In diesem Beispiel wird die Ausführung der Execute-Methode aus einem Command-Objekt und einem Connection-Objekt dargestellt. Außerdem wird die Requery-Methode zum Abrufen von aktuellen Daten in einem Recordset-Objekt und die Clear-Methode zum Löschen des Inhalts der Errors-Auflistung verwendet. (Auf die Errors-Auflistung wird mithilfe des Connection-Objekts der ActiveConnection-Eigenschaft des Recordset-Objekts zugegriffen.) Die Prozeduren ExecuteCommand und PrintOutput sind erforderlich, damit dieser Vorgang ausgeführt werden kann.

```vb 
 
'BeginExecuteVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo Err_Execute 
 
 ' connection, command, and recordset variables 
 Dim Cnxn As ADODB.Connection 
 Dim cmdChange As ADODB.Command 
 Dim rstTitles As ADODB.Recordset 
 Dim Err As ADODB.Error 
 Dim strSQLChange As String 
 Dim strSQLRestore As String 
 Dim strSQLTitles 
 Dim strCnxn As String 
 
 ' Define two SQL statements to execute as command text 
 strSQLChange = "UPDATE Titles SET Type = 'self_help' WHERE Type = 'psychology'" 
 strSQLRestore = "UPDATE Titles SET Type = 'psychology' WHERE Type = 'self_help'" 
 
 ' Open connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' Create command object 
 Set cmdChange = New ADODB.Command 
 Set cmdChange.ActiveConnection = Cnxn 
 cmdChange.CommandText = strSQLChange 
 
 ' Open titles table 
 Set rstTitles = New ADODB.Recordset 
 strSQLTitles = "titles" 
 rstTitles.Open strSQLTitles, Cnxn, , , adCmdTable 
 
 ' Print report of original data 
 Debug.Print _ 
 "Data in Titles table before executing the query" 
 PrintOutput rstTitles 
 
 ' Call the ExecuteCommand subroutine below to execute cmdChange command 
 ExecuteCommand cmdChange, rstTitles 
 
 ' Print report of new data 
 Debug.Print _ 
 "Data in Titles table after executing the query" 
 PrintOutput rstTitles 
 
 ' Use the Connection object's execute method to 
 ' execute SQL statement to restore data and trap for 
 ' errors, checking the Errors collection if necessary 
 Cnxn.Execute strSQLRestore, , adExecuteNoRecords 
 
 ' Retrieve the current data by requerying the recordset 
 rstTitles.Requery 
 
 ' Print report of restored data using sub from below 
 Debug.Print "Data after executing the query to restore the original information " 
 PrintOutput rstTitles 
 
 ' clean up 
 rstTitles.Close 
 Cnxn.Close 
 Set rstTitles = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
Err_Execute: 
 ' Notify user of any errors that result from 
 ' executing the query 
 If rstTitles.ActiveConnection.Errors.Count >= 0 Then 
 For Each Err In rstTitles.ActiveConnection.Errors 
 MsgBox "Error number: " & Err.Number & vbCr & _ 
 Err.Description 
 Next Err 
 End If 
 
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
 
Public Sub ExecuteCommand(cmdTemp As ADODB.Command, rstTemp As ADODB.Recordset) 
 
 Dim Err As Error 
 
 ' Run the specified Command object and trap for 
 ' errors, checking the Errors collection 
 On Error GoTo Err_Execute 
 cmdTemp.Execute 
 On Error GoTo 0 
 
 ' Retrieve the current data by requerying the recordset 
 rstTemp.Requery 
 
 Exit Sub 
 
Err_Execute: 
 
 ' Notify user of any errors that result from 
 ' executing the query 
 If rstTemp.ActiveConnection.Errors.Count > 0 Then 
 For Each Err In rstTemp.ActiveConnection.Errors 
 MsgBox "Error number: " & Err.Number & vbCr & _ 
 Err.Description 
 Next Err 
 End If 
 
 Resume Next 
 
End Sub 
 
Public Sub PrintOutput(rstTemp As ADODB.Recordset) 
 
 ' Enumerate Recordset 
 Do While Not rstTemp.EOF 
 Debug.Print " " & rstTemp!Title & _ 
 ", " & rstTemp!Type 
 rstTemp.MoveNext 
 Loop 
 
End Sub 
'EndExecuteVB 
```
