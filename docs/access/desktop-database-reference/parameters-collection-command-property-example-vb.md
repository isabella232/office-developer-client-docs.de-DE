---
<span data-ttu-id="2a0ac-101"><<<<<<< HEAD-Titel: Parameters-Auflistung, Command-Eigenschaft Beispiel) (VB) TOCTitle: Parameters-Auflistung, Command-Eigenschaft Beispiel) (VB) === Titel: Parameters-Auflistung, Command-Eigenschaft (Beispiel) (VB) TOCTitle: Parameter Auflistung, Command-Eigenschaft (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="2a0ac-101"><<<<<<< HEAD title: Parameters Collection, Command Property Example (VB) TOCTitle: Parameters Collection, Command Property Example (VB) ======= title: Parameters Collection, Command property example (VB) TOCTitle: Parameters Collection, Command property example (VB)</span></span>
>>>>>>> <span data-ttu-id="2a0ac-102">Master Ms:assetid: 3bb3e6e1-0ee5-70bb-7f2c-beb461d3914a Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249151(v=office.15) Ms:contentKeyID: 48544290 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="2a0ac-102">master ms:assetid: 3bb3e6e1-0ee5-70bb-7f2c-beb461d3914a ms:mtpsurl: https://msdn.microsoft.com/library/JJ249151(v=office.15) ms:contentKeyID: 48544290 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="2a0ac-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="2a0ac-103"><<<<<<< HEAD</span></span>
# <a name="parameters-collection-command-property-example-vb"></a><span data-ttu-id="2a0ac-104">Parameters-Auflistung, Command-Eigenschaft (VB-Beispiel)</span><span class="sxs-lookup"><span data-stu-id="2a0ac-104">Parameters Collection, Command Property Example (VB)</span></span>
=======
# <a name="parameters-collection-command-property-example-vb"></a><span data-ttu-id="2a0ac-105">Parameters-Auflistung, Command-Eigenschaft (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="2a0ac-105">Parameters Collection, Command property example (VB)</span></span>
>>>>>>> <span data-ttu-id="2a0ac-106">master</span><span class="sxs-lookup"><span data-stu-id="2a0ac-106">master</span></span>


<span data-ttu-id="2a0ac-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2a0ac-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2a0ac-108">Im folgenden Codebeispiel wird die Verwendung der [Command](command-property-adox.md)-Eigenschaft mit dem [Command](command-object-ado.md)-Objekt veranschaulicht, um Parameterinformationen für die Prozedur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="2a0ac-108">The following code demonstrates how to use the [Command](command-property-adox.md) property with the [Command](command-object-ado.md) object to retrieve parameter information for the procedure.</span></span>

```vb 
 
' BeginParametersVB 
Sub Main() 
 On Error GoTo ProcedureParametersError 
 
 Dim cnn As New ADODB.Connection 
 Dim cmd As ADODB.Command 
 Dim prm As ADODB.Parameter 
 Dim cat As New ADOX.Catalog 
 
 ' Open the Connection 
 cnn.Open _ 
 "Provider='Microsoft.Jet.OLEDB.4.0';" & _ 
 "Data Source='c:\Program Files\Microsoft Office\" & _ 
 "Office\Samples\Northwind.mdb';" 
 
 ' Open the catalog 
 Set cat.ActiveConnection = cnn 
 
 ' Get the command object 
 Set cmd = cat.Procedures("CustomerById").Command 
 
 ' Retrieve Parameter information 
 cmd.Parameters.Refresh 
 For Each prm In cmd.Parameters 
 Debug.Print prm.Name & ":" & prm.Type 
 Next 
 
 'Clean up 
 cnn.Close 
 Set cat = Nothing 
 Set cmd = Nothing 
 Set cnn = Nothing 
 Exit Sub 
 
ProcedureParametersError: 
 
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
' EndParametersVB 
```

