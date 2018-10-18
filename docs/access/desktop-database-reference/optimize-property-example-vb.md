---
<<<<<<< HEAD-Titel: Optimieren der Eigenschaft Beispiel) (VB) TOCTitle: Optimieren der Eigenschaft Beispiel) (VB) === Titel: optimieren-Eigenschaft (Beispiel) (VB) TOCTitle: optimieren-Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: f4576247-6057-c1fe-013d-74feaab33174 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250240(v=office.15) Ms:contentKeyID: 48548686 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="optimize-property-example-vb"></a>Optimize-Eigenschaft (Beispiel) (VB)
=======
# <a name="optimize-property-example-vb"></a>Optimieren der Eigenschaft (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Dieses Beispiel veranschaulicht die [Feld](field-object-ado.md) Objekte dynamische Optimize-Eigenschaft. Das ***Zip*** -Feld der ***Authors*** -Tabelle in der ***Pubs*** -Datenbank wird nicht indiziert. [Optimize](optimize-property-dynamic-ado.md) -Eigenschaft auf **True** festlegen, im Feld ***Zip*** autorisiert ADO einen Index zu erstellen, der die [Find](find-method-ado.md) -Methode die Leistung verbessert.

```vb 
 
'BeginOptimizeVB 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
 ' recordset and connection variables 
 Dim Cnxn As ADODB.Connection 
 Dim rstAuthors As ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 
 ' Open connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Set Cnxn = New ADODB.Connection 
 Cnxn.Open strCnxn 
 
 ' open recordset client-side to enable index creation 
 Set rstAuthors = New ADODB.Recordset 
 rstAuthors.CursorLocation = adUseClient 
 strSQLAuthors = "SELECT * FROM Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 ' Create the index 
 rstAuthors!zip.Properties("Optimize") = True 
 ' Find Akiko Yokomoto 
 rstAuthors.Find "zip = '94595'" 
 
 ' show results 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname & " " & _ 
 rstAuthors!address & " " & rstAuthors!city & " " & rstAuthors!State 
 rstAuthors!zip.Properties("Optimize") = False 'Delete the index 
 
 ' clean up 
 rstAuthors.Close 
 Cnxn.Close 
 Set rstAuthors = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstAuthors Is Nothing Then 
 If rstAuthors.State = adStateOpen Then rstAuthors.Close 
 End If 
 Set rstAuthors = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndOptimizeVB 
```

