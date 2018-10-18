---
<span data-ttu-id="9101e-101"><<<<<<< HEAD-Titel: SortOrder-Eigenschaft Beispiel) (VB) TOCTitle: SortOrder-Eigenschaft Beispiel) (VB) === Titel: SortOrder-Eigenschaft (Beispiel) (VB) TOCTitle: SortOrder-Eigenschaft (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="9101e-101"><<<<<<< HEAD title: SortOrder Property Example (VB) TOCTitle: SortOrder Property Example (VB) ======= title: SortOrder property example (VB) TOCTitle: SortOrder property example (VB)</span></span>
>>>>>>> <span data-ttu-id="9101e-102">Master Ms:assetid: 97937644-e3ef-06dc-d8ba-55ecaf7ac1ad Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249675(v=office.15) Ms:contentKeyID: 48546472 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="9101e-102">master ms:assetid: 97937644-e3ef-06dc-d8ba-55ecaf7ac1ad ms:mtpsurl: https://msdn.microsoft.com/library/JJ249675(v=office.15) ms:contentKeyID: 48546472 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="9101e-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="9101e-103"><<<<<<< HEAD</span></span>
# <a name="sortorder-property-example-vb"></a><span data-ttu-id="9101e-104">SortOrder-Eigenschaft (VB-Beispiel)</span><span class="sxs-lookup"><span data-stu-id="9101e-104">SortOrder Property Example (VB)</span></span>
=======
# <a name="sortorder-property-example-vb"></a><span data-ttu-id="9101e-105">SortOrder-Eigenschaft (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="9101e-105">SortOrder property example (VB)</span></span>
>>>>>>> <span data-ttu-id="9101e-106">master</span><span class="sxs-lookup"><span data-stu-id="9101e-106">master</span></span>

<span data-ttu-id="9101e-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="9101e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="9101e-p101">In diesem Beispiel wird die Verwendung der SortOrder-Eigenschaft eines Column-Objekts veranschaulicht, das an die Columns-Auflistung eines Index-Objekts angefügt wurde. Der Code fügt einen aufsteigenden Index an die Country-Spalte in der Employees-Tabelle an und zeigt dann die Datensätze an. Dann fügt der Code einen absteigenden Index an die Country-Spalte der Employees-Tabelle an und zeigt die Datensätze erneut an. Hierdurch wird der Unterschied zwischen aufsteigenden und absteigenden Indizes veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="9101e-p101">This example demonstrates the [SortOrder](sortorder-property-adox.md) property of a [Column](column-object-adox.md) that has been appended to the [Columns](columns-collection-adox.md) collection of an [Index](index-object-adox.md). The code appends an ascending index to the Country column in the **Employees** table, then displays the records. Then the code appends a descending index to the Country column in the **Employees** table and displays the records again. The difference between ascending and descending indexes is shown.</span></span>


```vb 
 
' BeginSortOrderVB 
Sub Main() 
 On Error GoTo SortOrderXError 
 
 Dim cnn As New ADODB.Connection 
 Dim catNorthwind As New ADOX.Catalog 
 Dim idxAscending As New ADOX.Index 
 Dim idxDescending As New ADOX.Index 
 Dim rstEmployees As New ADODB.Recordset 
 
 ' Connect the catalog. 
 cnn.Open "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\" & _ 
 "Microsoft Office\Office\Samples\Northwind.mdb';" 
 Set catNorthwind.ActiveConnection = cnn 
 
 ' Append Country column to new index 
 idxAscending.Columns.Append "Country" 
 idxAscending.Columns("Country").SortOrder = adSortAscending 
 idxAscending.Name = "Ascending" 
 idxAscending.IndexNulls = adIndexNullsAllow 
 
 'Append new index to Employees table 
 catNorthwind.Tables("Employees").Indexes.Append idxAscending 
 
 rstEmployees.Index = idxAscending.Name 
 rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
 adLockOptimistic, adCmdTableDirect 
 
 With rstEmployees 
 .MoveFirst 
 Debug.Print "Index = " & .Index 
 Debug.Print " Country - Name" 
 
 ' Enumerate the Recordset. The value of the 
 ' IndexNulls property will determine if the newly 
 ' added record appears in the output. 
 Do While Not .EOF 
 Debug.Print " " & !Country & " - " & _ 
 !FirstName & " " & !LastName 
 .MoveNext 
 Loop 
 
 .Close 
 End With 
 
 ' Append Country column to new index 
 idxDescending.Columns.Append "Country" 
 idxDescending.Columns("Country").SortOrder = adSortDescending 
 idxDescending.Name = "Descending" 
 idxDescending.IndexNulls = adIndexNullsAllow 
 
 'Append descending index to Employees table 
 catNorthwind.Tables("Employees").Indexes.Append idxDescending 
 
 rstEmployees.Index = idxDescending.Name 
 rstEmployees.Open "Employees", cnn, adOpenKeyset, _ 
 adLockOptimistic, adCmdTableDirect 
 
 With rstEmployees 
 .MoveFirst 
 Debug.Print "Index = " & .Index 
 Debug.Print " Country - Name" 
 
 ' Enumerate the Recordset. The value of the 
 ' IndexNulls property will determine if the newly 
 ' added record appears in the output. 
 Do While Not .EOF 
 Debug.Print " " & !Country & " - " & _ 
 !FirstName & " " & !LastName 
 .MoveNext 
 Loop 
 
 .Close 
 End With 
 
 ' Delete new Indexes because this is a demonstration. 
 catNorthwind.Tables("Employees").Indexes.Delete idxAscending.Name 
 catNorthwind.Tables("Employees").Indexes.Delete idxDescending.Name 
 
 'Clean up 
 cnn.Close 
 Set catNorthwind = Nothing 
 Set idxAscending = Nothing 
 Set idxDescending = Nothing 
 Set rstEmployees = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
SortOrderXError: 
 
 Set catNorthwind = Nothing 
 Set idxAscending = Nothing 
 Set idxDescending = Nothing 
 
 If Not rstEmployees Is Nothing Then 
 If rstEmployees.State = adStateOpen Then rstEmployees.Close 
 End If 
 Set rstEmployees = Nothing 
 
 If Not cnn Is Nothing Then 
 If cnn.State = adStateOpen Then cnn.Close 
 End If 
 Set cnn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
' EndSortOrderVB 
```

