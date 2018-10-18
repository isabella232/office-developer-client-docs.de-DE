---
<<<<<<< HEAD-Titel: Keys-Methode Append, Schlüsseltyp, RelatedColumn-Eigenschaften Beispiel) (VB) TOCTitle: Schlüssel Append-Methode, Schlüsseltyp, RelatedColumn-, RelatedTable- und UpdateRule Eigenschaften Beispiel) (VB) === Titel: Schlüssel Append-Methode, Schlüssel Typ, RelatedColumn-Eigenschaft (Beispiel) (VB) TOCTitle: Schlüssel Append-Methode, Schlüsseltyp, RelatedColumn-, RelatedTable- und UpdateRule-Eigenschaften (Beispiel) (VB)
>>>>>>> Master Ms:assetid: d1b0508d-ab2c-eece-061c-09c67ea9ecae Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250047(v=office.15) Ms:contentKeyID: 48547871 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a>Append-Methode (Keys), Key Type-, RelatedColumn-, RelatedTable- und UpdateRule-Eigenschaft (VB-Beispiel)
=======
# <a name="keys-append-method-key-type-relatedcolumn-relatedtable-and-updaterule-properties-example-vb"></a>Keys-Methode Append, Schlüsseltyp, RelatedColumn-, RelatedTable- und UpdateRule-Eigenschaften (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Im folgenden Code wird das Erstellen eines neuen Fremdschlüssels veranschaulicht. Es wird davon ausgegangen, dass zwei Tabellen (**Customers** und **Orders**) vorhanden sind.

```vb 
 
' BeginCreateKeyVB 
Sub Main() 
 On Error GoTo CreateKeyError 
 
 Dim kyForeign As New ADOX.Key 
 Dim cat As New ADOX.Catalog 
 
 ' Connect the catalog 
 cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Define the foreign key 
 kyForeign.Name = "CustOrder" 
 kyForeign.Type = adKeyForeign 
 kyForeign.RelatedTable = "Customers" 
 kyForeign.Columns.Append "CustomerId" 
 kyForeign.Columns("CustomerId").RelatedColumn = "CustomerId" 
 kyForeign.UpdateRule = adRICascade 
 
 ' Append the foreign key 
 cat.Tables("Orders").Keys.Append kyForeign 
 
 'Delete the Key as this is a demonstration 
 cat.Tables("Orders").Keys.Delete kyForeign.Name 
 
 'Clean up 
 Set cat.ActiveConnection = Nothing 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 Exit Sub 
 
CreateKeyError: 
 Set cat = Nothing 
 Set kyForeign = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
' EndCreateKeyVB 
```

