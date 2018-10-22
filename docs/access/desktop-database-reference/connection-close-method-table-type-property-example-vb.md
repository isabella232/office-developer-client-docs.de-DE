---
<<<<<<< HEAD-Titel: Connection Close-Methode, Tabelle Typ Eigenschaft Beispiel) (VB) TOCTitle: Connection Close-Methode, Tabelle Type-Eigenschaft Beispiel) (VB) === Titel: Connection Close-Methode vom Tabellentyp-Eigenschaft (Beispiel) (VB) TOCTitle: Connection Close-Methode vom Tabellentyp-Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: cd0bb6ad-af7b-fb9c-d45c-5d4b62459c03 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ250019(v=office.15) Ms:contentKeyID: 48547754 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="connection-close-method-table-type-property-example-vb"></a>Connection Close-Methode, Type-Eigenschaft (Table) (VB-Beispiel)
=======
# <a name="connection-close-method-table-type-property-example-vb"></a>Connection Close-Methode vom Tabellentyp-Eigenschaft (Beispiel) (VB)
>>>>>>> master

**Betrifft**: Access 2013 | Office 2013

Durch Festlegen der [ActiveConnection](activeconnection-property-adox.md)-Eigenschaft auf **Nothing** sollte der Katalog geschlossen werden. Verknüpfte Auflistungen sind leer. Alle Objekte, die von Schemaobjekten im Katalog erstellt wurden, werden verwaist. Alle zwischengespeicherten Eigenschaften für diese Objekte sind noch verfügbar. Bei dem Versuch, Eigenschaften zu lesen, die einen Aufruf des Anbieters erfordern, tritt jedoch ein Fehler auf.

```vb 
 
    ' BeginCloseConnectionVB 
    Sub Main() 
    On Error GoTo CloseConnectionByNothingError 
    
    Dim cnn As New ADODB.Connection 
    Dim cat As New ADOX.Catalog 
    Dim tbl As ADOX.Table 
    
    cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
    "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
    "Office\Samples\Northwind.mdb';" 
    Set cat.ActiveConnection = cnn 
    Set tbl = cat.Tables(0) 
    Debug.Print tbl.Type ' Cache tbl.Type info 
    Set cat.ActiveConnection = Nothing 
    Debug.Print tbl.Type ' tbl is orphaned 
    ' Previous line will succeed if this was cached 
    Debug.Print tbl.Columns(0).DefinedSize 
    ' Previous line will fail if this info has not been cached 
    
    'Clean up 
    cnn.Close 
    Set cat = Nothing 
    Set cnn = Nothing 
    Exit Sub 
    
    CloseConnectionByNothingError: 
    Set cat = Nothing 
    
    If Not cnn Is Nothing Then 
    If cnn.State = adStateOpen Then cnn.Close 
    End If 
    Set cnn = Nothing 
    
    If Err <> 0 Then 
    MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
    End Sub 
    ' EndCloseConnectionVB 
```

<br/>

Das Schließen eines [Connection](connection-object-ado.md)-Objekts, das zum Öffnen des Katalogs verwendet wurde, sollte dieselbe Wirkung erzielen wie das Festlegen der **ActiveConnection** -Eigenschaft auf **Nothing**.

```vb
    Sub CloseConnection() 
     On Error GoTo CloseConnectionError 
     
     Dim cnn As New ADODB.Connection 
     Dim cat As New ADOX.Catalog 
     Dim tbl As ADOX.Table 
     
     cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
     "Data Source= 'c:\Program Files\Microsoft Office\" & _ 
     "Office\Samples\Northwind.mdb';" 
     Set cat.ActiveConnection = cnn 
     Set tbl = cat.Tables(0) 
     Debug.Print tbl.Type ' Cache tbl.Type info 
     cnn.Close 
     Debug.Print tbl.Type ' tbl is orphaned 
     ' Previous line will succeed if this was cached 
     Debug.Print tbl.Columns(0).DefinedSize 
     ' Previous line will fail if this info has not been cached 
     
     'Clean up 
     Set cat = Nothing 
     Set cnn = Nothing 
     Exit Sub 
     
    CloseConnectionError: 
     
     Set cat = Nothing 
     
     If Not cnn Is Nothing Then 
     If cnn.State = adStateOpen Then cnn.Close 
     End If 
     Set cnn = Nothing 
     
     If Err <> 0 Then 
     MsgBox Err.Source & "-->" & Err.Description, , "Error" 
     End If 
    End Sub 
    ' EndCloseConnection2VB
```