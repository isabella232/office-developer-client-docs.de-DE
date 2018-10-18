---
<<<<<<< HEAD-Titel: Katalog ActiveConnection-Eigenschaft Beispiel) (VB) TOCTitle: Katalog ActiveConnection-Eigenschaft Beispiel) (VB) === Titel: Katalog ActiveConnection-Eigenschaft (Beispiel) (VB) TOCTitle: Katalog ActiveConnection Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: 12a34091-e451-dbd1-e7f3-f794b84ee5b0 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248901(v=office.15) Ms:contentKeyID: 48543348 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="catalog-activeconnection-property-example-vb"></a>ActiveConnection-Eigenschaft (Catalog) (VB-Beispiel)
=======
# <a name="catalog-activeconnection-property-example-vb"></a>Katalog ActiveConnection-Eigenschaft (Beispiel) (VB)
>>>>>>> master

**Betrifft**: Access 2013 | Office 2013

Durch das Festlegen der [ActiveConnection](activeconnection-property-adox.md)-Einstellung auf eine gültige, offene Verbindung wird der Katalog geöffnet. Über einen geöffneten Katalog können Sie auf die Schemaobjekte zugreifen, die in dem jeweiligen Katalog enthalten sind.

```vb 
 
    ' BeginOpenConnectionVB 
    Sub OpenConnection() 
    On Error GoTo OpenConnectionError 
    
    Dim cnn As New ADODB.Connection 
    Dim cat As New ADOX.Catalog 
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
    "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
    "Office\Samples\Northwind.mdb';" 
    Set cat.ActiveConnection = cnn 
    Debug.Print cat.Tables(0).Type 
    
    'Clean up 
    cnn.Close 
    Set cat = Nothing 
    Set cnn = Nothing 
    Exit Sub 
    
    OpenConnectionError: 
    
    Set cat = Nothing 
    
    If Not cnn Is Nothing Then 
    If cnn.State = adStateOpen Then cnn.Close 
    End If 
    Set cnn = Nothing 
    
    If Err <> 0 Then 
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
    End Sub 
    ' EndOpenConnectionVB 
```

Der Katalog wird außerdem geöffnet, indem Sie die **ActiveConnection** -Eigenschaft auf eine gültige Verbindungszeichenfolge festlegen.

```vb
    ' BeginOpenConnection2VB 
    Sub Main() 
     On Error GoTo OpenConnectionWithStringError 
     Dim cat As New ADOX.Catalog 
     
     cat.ActiveConnection = "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source='c:\Program Files\Microsoft Office\" & _ 
     "Office\Samples\Northwind.mdb';" 
     Debug.Print cat.Tables(0).Type 
     
     'Clean up 
     Set cat.ActiveConnection = Nothing 
     Exit Sub 
     
    OpenConnectionWithStringError: 
     Set cat = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
    End Sub 
    ' EndOpenConnection2VB
```
