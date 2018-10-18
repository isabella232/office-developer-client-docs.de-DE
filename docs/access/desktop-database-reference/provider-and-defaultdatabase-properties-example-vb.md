---
<span data-ttu-id="b386e-101"><<<<<<< HEAD-Titel: Provider- und DefaultDatabase Eigenschaften Beispiel) (VB) TOCTitle: Provider- und DefaultDatabase Eigenschaften Beispiel) (VB) === Titel: Provider- und DefaultDatabase-Eigenschaften (Beispiel) (VB) TOCTitle: Anbieter und DefaultDatabase-Eigenschaften (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="b386e-101"><<<<<<< HEAD title: Provider and DefaultDatabase Properties Example (VB) TOCTitle: Provider and DefaultDatabase Properties Example (VB) ======= title: Provider and DefaultDatabase properties example (VB) TOCTitle: Provider and DefaultDatabase properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="b386e-102">Master Ms:assetid: 337b90e6-851d-2101-0671-50c4173aec13 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ249104(v=office.15) Ms:contentKeyID: 48544107 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="b386e-102">master ms:assetid: 337b90e6-851d-2101-0671-50c4173aec13 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249104(v=office.15) ms:contentKeyID: 48544107 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="b386e-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="b386e-103"><<<<<<< HEAD</span></span>
# <a name="provider-and-defaultdatabase-properties-example-vb"></a><span data-ttu-id="b386e-104">Provider- und DefaultDatabase-Eigenschaft (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="b386e-104">Provider and DefaultDatabase Properties Example (VB)</span></span>
=======
# <a name="provider-and-defaultdatabase-properties-example-vb"></a><span data-ttu-id="b386e-105">Provider- und DefaultDatabase-Eigenschaften (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="b386e-105">Provider and DefaultDatabase properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="b386e-106">master</span><span class="sxs-lookup"><span data-stu-id="b386e-106">master</span></span>


<span data-ttu-id="b386e-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b386e-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b386e-p101">Dieses Beispiel veranschaulicht die [Provider](provider-property-ado.md)-Eigenschaft, indem drei [Connection](connection-object-ado.md)-Objekte unter Verwendung verschiedener Anbieter geöffnet werden. Außerdem wird mit der [DefaultDatabase](defaultdatabase-property-ado.md)-Eigenschaft die Standarddatenbank für den Microsoft ODBC-Anbieter festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b386e-p101">This example demonstrates the [Provider](provider-property-ado.md) property by opening three [Connection](connection-object-ado.md) objects using different providers. It also uses the [DefaultDatabase](defaultdatabase-property-ado.md) property to set the default database for the Microsoft ODBC Provider.</span></span>

```vb 
 
'BeginProviderVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection strings 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 Dim Cnxn1 As ADODB.Connection 
 Dim Cnxn2 As ADODB.Connection 
 Dim Cnxn3 As ADODB.Connection 
 Dim strCnxn As String 
 
 ' Open a connection using the Microsoft ODBC provider 
 Set Cnxn1 = New ADODB.Connection 
 Cnxn1.ConnectionString = "driver={SQL Server};server='MySqlServer';" & _ 
 "user id='MyUserID';password='MyPassword';" 
 Cnxn1.Open strCnxn 
 Cnxn1.DefaultDatabase = "Pubs" 
 
 ' Display the provider 
 MsgBox "Cnxn1 provider: " & Cnxn1.Provider 
 
 ' Open a connection using the Microsoft Jet provider 
 Set Cnxn2 = New ADODB.Connection 
 Cnxn2.Provider = "Microsoft.Jet.OLEDB.4.0" 
 Cnxn2.Open "C:\Program Files\Microsoft Office\Office\Samples\northwind.mdb", _ 
 "MyUserID", "MyPassword" 
 
 ' Display the provider. 
 MsgBox "Cnxn2 provider: " & Cnxn2.Provider 
 
 ' Open a connection using the Microsoft SQL Server provider 
 Set Cnxn3 = New ADODB.Connection 
 Cnxn3.Provider = "sqloledb" 
 Cnxn3.Open "Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 
 ' Display the provider 
 MsgBox "Cnxn3 provider: " & Cnxn3.Provider 
 
 ' clean up 
 Cnxn1.Close 
 Cnxn2.Close 
 Cnxn3.Close 
 Set Cnxn1 = Nothing 
 Set Cnxn2 = Nothing 
 Set Cnxn3 = Nothing 
 Exit Sub 
 
ErrorHandler: 
 If Not Cnxn1 Is Nothing Then 
 If Cnxn1.State = adStateOpen Then Cnxn1.Close 
 End If 
 Set Cnxn1 = Nothing 
 
 If Not Cnxn2 Is Nothing Then 
 If Cnxn2.State = adStateOpen Then Cnxn2.Close 
 End If 
 Set Cnxn2 = Nothing 
 
 If Not Cnxn3 Is Nothing Then 
 If Cnxn3.State = adStateOpen Then Cnxn3.Close 
 End If 
 Set Cnxn3 = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndProviderVB 
```

