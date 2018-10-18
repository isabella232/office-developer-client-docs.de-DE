---
<<<<<<< HEAD-Titel: DeleteRule-Eigenschaft Beispiel) (VB) TOCTitle: DeleteRule-Eigenschaft Beispiel) (VB) === Titel: DeleteRule-Eigenschaft (Beispiel) (VB) TOCTitle: DeleteRule-Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: 354e00b6-cecb-1132-6923-fc9e8853fa0e Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249114(v=office.15) Ms:contentKeyID: 48544142 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="deleterule-property-example-vb"></a>DeleteRule-Eigenschaft (VB-Beispiel)
=======
# <a name="deleterule-property-example-vb"></a>DeleteRule-Eigenschaft (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

In diesem Beispiel wird die Verwendung der [DeleteRule](deleterule-property-adox.md)-Eigenschaft eines [Key](key-object-adox.md)-Objekts veranschaulicht. Der Code fügt ein neues [Table](table-object-adox.md)-Objekt an und definiert dann einen neuen Primärschlüssel, indem **DeleteRule** auf **adRICascade** festgelegt wird.

```vb 
 
' BeginDeleteRuleVB 
Sub Main() 
 On Error GoTo DeleteRuleXError 
 
 Dim kyPrimary As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 Dim tblNew As New ADOX.Table 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "data source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 
 ' Name new table 
 tblNew.Name = "NewTable" 
 
 ' Append a numeric and a text field to new table. 
 tblNew.Columns.Append "NumField", adInteger, 20 
 tblNew.Columns.Append "TextField", adVarWChar, 20 
 
 ' Append the new table 
 cat.Tables.Append tblNew 
 
 ' Define the Primary key 
 kyPrimary.Name = "NumField" 
 kyPrimary.Type = adKeyPrimary 
 kyPrimary.RelatedTable = "Customers" 
 kyPrimary.Columns.Append "NumField" 
 kyPrimary.Columns("NumField").RelatedColumn = "CustomerId" 
 kyPrimary.DeleteRule = adRICascade 
 
 ' Append the primary key 
 cat.Tables("NewTable").Keys.Append kyPrimary 
 Debug.Print "The primary key is appended." 
 
 'Delete the table as this is a demonstration. 
 cat.Tables.Delete tblNew.Name 
 Debug.Print "The primary key is deleted." 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 Exit Sub 
 
DeleteRuleXError: 
 
 Set cat = Nothing 
 Set kyPrimary = Nothing 
 Set tblNew = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndDeleteRuleVB 
```

