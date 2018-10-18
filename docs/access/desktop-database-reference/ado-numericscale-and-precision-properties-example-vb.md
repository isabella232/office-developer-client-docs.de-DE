---
<span data-ttu-id="e2caf-101"><<<<<<< HEAD-Titel: ADO NumericScale- und Precision Eigenschaften Beispiel) (VB) TOCTitle: NumericScale- und Precision Eigenschaften Beispiel) (VB) === Titel: ADO NumericScale- und Precision-Eigenschaften (Beispiel) (VB) TOCTitle: NumericScale und Precision-Eigenschaft (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="e2caf-101"><<<<<<< HEAD title: ADO NumericScale and Precision Properties Example (VB) TOCTitle: NumericScale and Precision Properties Example (VB) ======= title: ADO NumericScale and Precision properties example (VB) TOCTitle: NumericScale and Precision properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="e2caf-102">Master Ms:assetid: 060394b1-0c2c-3726-92a0-0f350bbaa3d5 Ms:mtpsurl: https://msdn.microsoft.com/library/JJ248814(v=office.15) Ms:contentKeyID: 48543044 ms.date: 09/18/2015 Mtps_version: Office. 15</span><span class="sxs-lookup"><span data-stu-id="e2caf-102">master ms:assetid: 060394b1-0c2c-3726-92a0-0f350bbaa3d5 ms:mtpsurl: https://msdn.microsoft.com/library/JJ248814(v=office.15) ms:contentKeyID: 48543044 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="e2caf-103"><<<<<<< Kopf</span><span class="sxs-lookup"><span data-stu-id="e2caf-103"><<<<<<< HEAD</span></span>
# <a name="ado-numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="e2caf-104">ADO NumericScale and Precision Properties Example (VB)</span><span class="sxs-lookup"><span data-stu-id="e2caf-104">ADO NumericScale and Precision Properties Example (VB)</span></span>
=======
# <a name="ado-numericscale-and-precision-properties-example-vb"></a><span data-ttu-id="e2caf-105">ADO NumericScale- und Precision-Eigenschaften (Beispiel) (VB)</span><span class="sxs-lookup"><span data-stu-id="e2caf-105">ADO NumericScale and Precision properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="e2caf-106">master</span><span class="sxs-lookup"><span data-stu-id="e2caf-106">master</span></span>


<span data-ttu-id="e2caf-107">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e2caf-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e2caf-108">In diesem Beispiel werden die Eigenschaften [NumericScale](numericscale-property-ado.md) und [Precision](precision-property-ado.md) verwendet, um die Anzahl von Dezimalstellen und die Genauigkeit der Felder in der ***Discounts***-Tabelle der ***Pubs***-Datenbank anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e2caf-108">This example uses the [NumericScale](numericscale-property-ado.md) and [Precision](precision-property-ado.md) properties to display the numeric scale and precision of fields in the ***Discounts*** table of the ***Pubs*** database.</span></span>

```vb 
 
'BeginNumericScaleVB 
 
 'To integrate this code 
 'replace the data source and initial catalog values 
 'in the connection string 
 
Public Sub Main() 
 On Error GoTo ErrorHandler 
 
 ' connection and recordset variables 
 Dim rstDiscounts As ADODB.Recordset 
 Dim Cnxn As ADODB.Connection 
 Dim fldTemp As ADODB.Field 
 Dim strCnxn As String 
 Dim strSQLDiscounts As String 
 
 ' Open connection 
 Set Cnxn = New ADODB.Connection 
 strCnxn = "Provider='sqloledb';Data Source='MySqlServer';" & _ 
 "Initial Catalog='Pubs';Integrated Security='SSPI';" 
 Cnxn.Open strCnxn 
 
 ' Open recordset 
 Set rstDiscounts = New ADODB.Recordset 
 strSQLDiscounts = "Discounts" 
 rstDiscounts.Open strSQLDiscounts, Cnxn, adOpenStatic, adLockReadOnly, adCmdTable 
 
 ' Display numeric scale and precision of 
 ' numeric and small integer fields 
 For Each fldTemp In rstDiscounts.Fields 
 If fldTemp.Type = adNumeric Or fldTemp.Type = adSmallInt Then 
 MsgBox "Field: " & fldTemp.Name & vbCr & _ 
 "Numeric scale: " & _ 
 fldTemp.NumericScale & vbCr & _ 
 "Precision: " & fldTemp.Precision 
 End If 
 Next fldTemp 
 
 ' clean up 
 rstDiscounts.Close 
 Cnxn.Close 
 Set rstDiscounts = Nothing 
 Set Cnxn = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not rstDiscounts Is Nothing Then 
 If rstDiscounts.State = adStateOpen Then rstDiscounts.Close 
 End If 
 Set rstDiscounts = Nothing 
 
 If Not Cnxn Is Nothing Then 
 If Cnxn.State = adStateOpen Then Cnxn.Close 
 End If 
 Set Cnxn = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
 
End Sub 
'EndNumericScaleVB 
```

