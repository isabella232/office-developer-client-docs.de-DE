---
<<<<<<< HEAD-Titel: ParentCatalog-Eigenschaft Beispiel) (VB) TOCTitle: ParentCatalog-Eigenschaft Beispiel) (VB) === Titel: ParentCatalog-Eigenschaft (Beispiel) (VB) TOCTitle: ParentCatalog-Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: 3bd01153-40b5-1a45-67e2-eb8154c3fe33 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249152(v=office.15) Ms:contentKeyID: 48544295 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="parentcatalog-property-example-vb"></a>ParentCatalog-Eigenschaft (VB-Beispiel)
=======
# <a name="parentcatalog-property-example-vb"></a>ParentCatalog-Eigenschaft (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Im folgenden Codebeispiel wird die Verwendung der ParentCatalog-Eigenschaft veranschaulicht, um vor dem Anfügen einer Tabelle an einen Katalog auf eine anbieterspezifische Eigenschaft zuzugreifen. Die Eigenschaft ist die AutoIncrement-Eigenschaft, die ein AutoIncrement-Feld in einer Microsoft Jet-Datenbank erstellt.

```vb 
 
' BeginCreateAutoIncrColumnVB 
Sub Main() 
 On Error GoTo CreateAutoIncrColumnError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tbl As New ADOX.Table 
 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set cat.ActiveConnection = cnn 
 
 With tbl 
 .Name = "MyContacts" 
 Set .ParentCatalog = cat 
 ' Create fields and append them to the new Table object. 
 .Columns.Append "ContactId", adInteger 
 ' Make the ContactId column and auto incrementing column 
 .Columns("ContactId").Properties("AutoIncrement") = True 
 .Columns.Append "CustomerID", adVarWChar 
 .Columns.Append "FirstName", adVarWChar 
 .Columns.Append "LastName", adVarWChar 
 .Columns.Append "Phone", adVarWChar, 20 
 .Columns.Append "Notes", adLongVarWChar 
 End With 
 
 cat.Tables.Append tbl 
 Debug.Print "Table 'MyContacts' is added." 
 
 ' Delete the table as this is a demonstration. 
 cat.Tables.Delete tbl.Name 
 Debug.Print "Table 'MyContacts' is delete." 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set tbl = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
CreateAutoIncrColumnError: 
 
 Set cat = Nothing 
 Set tbl = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateAutoIncrColumnVB 
```

