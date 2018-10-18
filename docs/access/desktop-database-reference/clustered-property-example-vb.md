---
<<<<<<< HEAD-Titel: gruppierte Eigenschaft Beispiel) (VB) TOCTitle: gruppierte Eigenschaft Beispiel) (VB) === Titel: Clustered-Eigenschaft (Beispiel) (VB) TOCTitle: Clustered-Eigenschaft (Beispiel) (VB)
>>>>>>> Master Ms:assetid: 1065622d-9473-209a-95be-c4b0ab5b687a Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248872(v=office.15) Ms:contentKeyID: 48543293 ms.date: 09/18/2015 Mtps_version: Office. 15
---

<<<<<<< Kopf
# <a name="clustered-property-example-vb"></a>Clustered-Eigenschaft (VB-Beispiel)
=======
# <a name="clustered-property-example-vb"></a>Clustered-Eigenschaft (Beispiel) (VB)
>>>>>>> master


**Betrifft**: Access 2013 | Office 2013

Dieses Beispiel veranschaulicht die [Clustered](clustered-property-adox.md) -Eigenschaft eines [Index](index-object-adox.md). Beachten Sie, dass Microsoft Jet-Datenbanken gruppierte Indizes nicht unterstützen, sodass in diesem Beispiel wird für alle Indizes in der *Nordwind* -Datenbank die **Clustered** -Eigenschaft **False** zurückgibt.

```vb 
 
' BeginClusteredVB 
Sub Main() 
 On Error GoTo ClusteredXError 
 
 Dim cnn As New ADODB.Connection 
 Dim cat As New ADOX.Catalog 
 Dim tblLoop As ADOX.Table 
 Dim idxLoop As ADOX.Index 
 Dim strCnn As String 
 
 strCnn = "Provider='SQLOLEDB';Data Source='MySqlServer';Initial Catalog='pubs';" & _ 
 "Integrated Security='SSPI';" 
 ' Connect the catalog. 
 cnn.Open strCnn 
 cat.ActiveConnection = cnn 
 
 ' Enumerate Tables 
 For Each tblLoop In cat.Tables 
 'Enumerate Indexes 
 For Each idxLoop In tblLoop.Indexes 
 Debug.Print tblLoop.Name & " " & _ 
 idxLoop.Name & " " & idxLoop.Clustered 
 Next idxLoop 
 Next tblLoop 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ClusteredXError: 
 
 Set cat = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndClusteredVB 
```

