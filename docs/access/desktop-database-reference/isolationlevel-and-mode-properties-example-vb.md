---
<<<<<<< HEAD-Titel: IsolationLevel- und Mode Eigenschaften Beispiel) (VB) TOCTitle: IsolationLevel- und Mode Eigenschaften Beispiel) (VB) === Titel: Eigenschaften IsolationLevel- und Mode (Beispiel) (VB) TOCTitle: IsolationLevel- und Mode Eigenschaften (Beispiel) (VB)
>>>>>>> Master Ms:assetid: ac3ec2e7-199c-723c-ff3e-2aaf3e10aa94 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249800(v=office.15) Ms:contentKeyID: 48546999 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="isolationlevel-and-mode-properties-example-vb"></a>IsolationLevel- und Mode-Eigenschaft (Beispiel) (VB)
=======
# <a name="isolationlevel-and-mode-properties-example-vb"></a>IsolationLevel- und Mode-Eigenschaften (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

In diesem Beispiel wird die [Mode](mode-property-ado.md)-Eigenschaft verwendet, um eine exklusive Verbindung zu öffnen, und mit der [Level](isolationlevel-property-ado.md)-Eigenschaft wird eine Transaktion geöffnet, die isoliert von anderen Transaktionen ausgeführt wird.

```vb 
 
'BeginIsolationLevelVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn As ADODB.Connection 
 Dim rstTitles As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLTitles As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Mode = adModeShareExclusive 
 Cnxn.IsolationLevel = adXactIsolated 
 Cnxn.Open strCnxn 
 
 ' open Titles table 
 Set rstTitles = New ADODB.Recordset 
 strSQLTitles = "titles" 
 rstTitles.Open strSQLTitles, Cnxn, adOpenDynamic, adLockPessimistic, adCmdTable 
 
 Cnxn.BeginTrans 
 
 ' Display connection mode 
 If Cnxn.Mode = adModeShareExclusive Then 
 MsgBox "Connection mode is exclusive." 
 Else 
 MsgBox "Connection mode is not exclusive." 
 End If 
 
 ' Display isolation level 
 If Cnxn.IsolationLevel = adXactIsolated Then 
 MsgBox "Transaction is isolated." 
 Else 
 MsgBox "Transaction is not isolated." 
 End If 
 
 ' Change the type of psychology titles 
 Do Until rstTitles.EOF 
 If Trim(rstTitles!Type) = "psychology" Then 
 rstTitles!Type = "self_help" 
 rstTitles.Update 
 End If 
 rstTitles.MoveNext 
 Loop 
 
 ' Print current data in recordset 
 rstTitles.Requery 
 Do While Not rstTitles.EOF 
 Debug.Print rstTitles!Title & " - " & rstTitles!Type 
 rstTitles.MoveNext 
 Loop 
 
 ' clean up 
 rstTitles.Close 
 Cnxn.RollbackTrans 
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
 If Cnxn.State = adStateOpen Then 
 Cnxn.RollbackTrans 
 Cnxn.Close 
 End If 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndIsolationLevelVB 
```

