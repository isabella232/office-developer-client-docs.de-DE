---
title: Field2.AllowZeroLength-Eigenschaft (DAO)
TOCTitle: AllowZeroLength Property
ms:assetid: d3795634-527f-b4c5-b606-50f9945cac12
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834791(v=office.15)
ms:contentKeyID: 48547908
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3125a5669ea8aa016d8554be0357572d56c08ecf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721178"
---
# <a name="field2allowzerolength-property-dao"></a><span data-ttu-id="b25c9-102">Field2.AllowZeroLength-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="b25c9-102">Field2.AllowZeroLength property (DAO)</span></span>


<span data-ttu-id="b25c9-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b25c9-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="b25c9-104">Gibt einen Wert zurück oder legt einen Wert fest, der angibt, ob eine leere Zeichenfolge ("") eine gültige Einstellung für die Value-Eigenschaft des Field2-Objekts mit einem Datentyp Text oder Memo ist (gilt nur für Microsoft Access-Arbeitsbereiche).</span><span class="sxs-lookup"><span data-stu-id="b25c9-104">Sets or returns a value that indicates whether a zero-length string ("") is a valid setting for the **[Value](field-value-property-dao.md)** property of the **Field2** object with a Text or Memo data type (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b25c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b25c9-105">Syntax</span></span>

<span data-ttu-id="b25c9-106">*Ausdruck* . AllowZeroLength</span><span class="sxs-lookup"><span data-stu-id="b25c9-106">*expression* .AllowZeroLength</span></span>

<span data-ttu-id="b25c9-107">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="b25c9-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b25c9-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b25c9-108">Remarks</span></span>

<span data-ttu-id="b25c9-109">Bei einem Objekt, das noch nicht der **Fields**-Auflistung angefügt wurde, besteht für diese Eigenschaft Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b25c9-109">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="b25c9-110">Nachdem die **AllowZeroLength**-Eigenschaft der **Fields**-Auflistung hinzugefügt wurde, hängt ihre Verfügbarkeit vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="b25c9-110">Once appended to a **Fields** collection, the availability of the **AllowZeroLength** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b25c9-111">Zugehörigkeit der Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="b25c9-111">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="b25c9-112">Verfügbarkeit von AllowZeroLength</span><span class="sxs-lookup"><span data-stu-id="b25c9-112">Then AllowZeroLength is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b25c9-113"><strong>Index</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="b25c9-113"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b25c9-114">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b25c9-114">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b25c9-115"><strong>QueryDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="b25c9-115"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b25c9-116">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b25c9-116">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b25c9-117"><strong>Recordset</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="b25c9-117"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b25c9-118">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="b25c9-118">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b25c9-119"><strong>Relation</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="b25c9-119"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b25c9-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b25c9-120">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b25c9-121"><strong>TableDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="b25c9-121"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b25c9-122">Lese-/Schreibzugriff</span><span class="sxs-lookup"><span data-stu-id="b25c9-122">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b25c9-123">Sie können diese Eigenschaft zusammen mit der Eigenschaft **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)** oder **[ValidationRule](field-validationrule-property-dao.md)** verwenden, um einen Wert in einem Feld zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="b25c9-123">You can use this property along with the **[Required](field-required-property-dao.md)**, **[ValidateOnSet](field-validateonset-property-dao.md)**, or **[ValidationRule](field-validationrule-property-dao.md)** property to validate a value in a field.</span></span>

## <a name="example"></a><span data-ttu-id="b25c9-124">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b25c9-124">Example</span></span>

<span data-ttu-id="b25c9-p101">In diesem Beispiel ermöglicht die **AllowZeroLength**-Eigenschaft dem Benutzer, den Wert eines **Field2**-Objekts auf eine leere Zeichenfolge festzulegen. Hierdurch können Benutzer zwischen einem Datensatz unterscheiden, für den keine Daten bekannt sind, und einem Datensatz, für den die Daten nicht angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="b25c9-p101">In this example, the **AllowZeroLength** property allows the user to set the value of a **Field2** to an empty string. In this situation, the user can distinguish between a record where data is not known and a record where the data does not apply.</span></span>

```vb
    Sub AllowZeroLengthX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldTemp As Field 
     Dim rstEmployees As Recordset 
     Dim strMessage As String 
     Dim strInput As String 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     ' Create a new Field object and append it to the Fields 
     ' collection of the Employees table. 
     Set fldTemp = tdfEmployees.CreateField("FaxPhone", _ 
     dbText, 24) 
     fldTemp.AllowZeroLength = True 
     tdfEmployees.Fields.Append fldTemp 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Get user input. 
     .Edit 
     strMessage = "Enter fax number for " & _ 
     !FirstName & " " & !LastName & "." & vbCr & _ 
     "[? - unknown, X - has no fax]" 
     strInput = UCase(InputBox(strMessage)) 
     If strInput <> "" Then 
     Select Case strInput 
     Case "?" 
     !FaxPhone = Null 
     Case "X" 
     !FaxPhone = "" 
     Case Else 
     !FaxPhone = strInput 
     End Select 
     
     .Update 
     
     ' Print report. 
     Debug.Print "Name - Fax number" 
     Debug.Print !FirstName & " " & !LastName & " - "; 
     
     If IsNull(!FaxPhone) Then 
     Debug.Print "[Unknown]" 
     Else 
     If !FaxPhone = "" Then 
     Debug.Print "[Has no fax]" 
     Else 
     Debug.Print !FaxPhone 
     End If 
     End If 
     
     Else 
     .CancelUpdate 
     End If 
     
     .Close 
     End With 
     
     ' Delete new field because this is a demonstration. 
     tdfEmployees.Fields.Delete fldTemp.Name 
     dbsNorthwind.Close 
     
    End Sub
```
