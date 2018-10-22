---
<<<<<<< HEAD-Titel: Sortieren Eigenschaft Beispiel) (VB) TOCTitle: Sortieren Eigenschaft Beispiel) (VB) === Titel: Sort-Eigenschaft (Beispiel) (VB) TOCTitle: Sort-Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: 6f981e5e-7ee8-e1e7-bea9-7c2081400391 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249440(v=office.15) Ms:contentKeyID: 48545539 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="sort-property-example-vb"></a>Sort-Eigenschaft (Beispiel) (VB)
=======
# <a name="sort-property-example-vb"></a>Sort-Eigenschaft (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

In diesem Beispiel wird die [Sort](sort-property-ado.md)-Eigenschaft des [Recordset](recordset-object-ado.md)-Objekts verwendet, um die Zeilen in einem **Recordset**-Objekt neu anzuordnen, das aus der ***Authors***-Tabelle der ***Pubs***-Datenbank stammt. Eine sekundäre Hilfsprogrammroutine druckt jede Zeile.

```vb 
 
'BeginSortVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim Cnxn As New ADODB.Connection 
 Dim rstAuthors As New ADODB.Recordset 
 Dim strCnxn As String 
 Dim strSQLAuthors As String 
 
 Dim strTitle As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' open client-side recordset to enable sort method 
 Set rstAuthors = New ADODB.Recordset 
 rstAuthors.CursorLocation = adUseClient 
 strSQLAuthors = "SELECT * FROM Authors" 
 rstAuthors.Open strSQLAuthors, Cnxn, adOpenStatic, adLockReadOnly, adCmdText 
 
 ' sort the recordset last name ascending 
 rstAuthors.Sort = "au_lname ASC, au_fname ASC" 
 ' show output 
 Debug.Print "Last Name Ascending:" 
 Debug.Print "First Name Last Name" & vbCr 
 
 rstAuthors.MoveFirst 
 Do Until rstAuthors.EOF 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname 
 rstAuthors.MoveNext 
 Loop 
 
 ' sort the recordset last name descending 
 rstAuthors.Sort = "au_lname DESC, au_fname ASC" 
 ' show output 
 Debug.Print "Last Name Descending" 
 Debug.Print "First Name Last Name" & vbCr 
 
 Do Until rstAuthors.EOF 
 Debug.Print rstAuthors!au_fname & " " & rstAuthors!au_lname 
 rstAuthors.MoveNext 
 Loop 
 
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
'EndSortVB 
```

Das ist die sekundäre Hilfsprogrammroutine, die den angegebenen Titel und den Inhalt des angegebenen **Recordset** -Objekts druckt.

```vb 
 
Attribute VB_Name = "Sort" 
```
