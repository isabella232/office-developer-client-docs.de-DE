---
<<<<<<< HEAD-Titel: Views-Auflistung, CommandText-Eigenschaft Beispiel) (VB) TOCTitle: Views-Auflistung, CommandText-Eigenschaft Beispiel) (VB) === Titel: Views-Auflistung, CommandText-Eigenschaft (Beispiel) (VB) TOCTitle: Views-Auflistung CommandText-Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: 5dacd3c2-a1b2-57a7-1bac-ce0caa7c1a09 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249331(v=office.15) Ms:contentKeyID: 48545120 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="views-collection-commandtext-property-example-vb"></a>Views-Auflistung, CommandText-Eigenschaft (VB-Beispiel)
=======
# <a name="views-collection-commandtext-property-example-vb"></a>Views-Auflistung, CommandText-Eigenschaft (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Im folgenden Codebeispiel wird die Verwendung der [Command](command-property-adox.md)-Eigenschaft veranschaulicht, um den Text einer Sicht zu aktualisieren.

```vb 
 
' BeginViewsCollectionVB 
Sub Main() 
 On Error GoTo ViewTextError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim cmd As New ADODB.Command 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command 
 Set cmd = cat.Views("AllCustomers").Command 
 
 ' Update the CommandText of the Command 
 cmd.CommandText = _ 
 "Select CustomerId, CompanyName, ContactName From Customers" 
 
 ' Update the View 
 Set cat.Views("AllCustomers").Command = cmd 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ViewTextError: 
 
 Set cat = Nothing 
 Set cmd = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndViewsCollectionVB 
```
