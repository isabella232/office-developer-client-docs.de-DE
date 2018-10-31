---
title: Field.GetChunk Method (DAO)
TOCTitle: GetChunk Method
ms:assetid: b8984e79-54f7-8052-85a3-d12033daf7a1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822448(v=office.15)
ms:contentKeyID: 48547328
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052871
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 691b4d0b18b31c4c4a40f73e232a1829101913f1
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863276"
---
# <a name="fieldgetchunk-method-dao"></a><span data-ttu-id="27aff-102">Field.GetChunk Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="27aff-102">Field.GetChunk Method (DAO)</span></span>


<span data-ttu-id="27aff-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="27aff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="27aff-104">Gibt den gesamten Inhalt oder einen Teil des Inhalts eines \*\*\*\*Field\*\*\*\* -Objekts vom Typ [Memo](field-object-dao.md) oder **Long Binary** in der **[Fields](fields-collection-dao.md)** -Auflistung eines **[Recordset](recordset-object-dao.md)** -Objekts zurück.</span><span class="sxs-lookup"><span data-stu-id="27aff-104">Returns all or a portion of the contents of a **Memo** or **Long Binary** **[Field](field-object-dao.md)** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="27aff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="27aff-105">Syntax</span></span>

<span data-ttu-id="27aff-106">*Ausdruck* . GetChunk (***Offset***, ***Byte***)</span><span class="sxs-lookup"><span data-stu-id="27aff-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="27aff-107">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="27aff-107">*expression* A variable that represents a **Field** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="27aff-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="27aff-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27aff-109">Name</span><span class="sxs-lookup"><span data-stu-id="27aff-109">Name</span></span></p></th>
<th><p><span data-ttu-id="27aff-110">Erforderlich/Optional</span><span class="sxs-lookup"><span data-stu-id="27aff-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="27aff-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="27aff-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="27aff-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27aff-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27aff-113">Offset</span><span class="sxs-lookup"><span data-stu-id="27aff-113">Offset</span></span></p></td>
<td><p><span data-ttu-id="27aff-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="27aff-114">Required</span></span></p></td>
<td><p><span data-ttu-id="27aff-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="27aff-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="27aff-116">Die Anzahl von zu überspringenden Bytes, bevor das Kopieren gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="27aff-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27aff-117">Bytes</span><span class="sxs-lookup"><span data-stu-id="27aff-117">Bytes</span></span></p></td>
<td><p><span data-ttu-id="27aff-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="27aff-118">Required</span></span></p></td>
<td><p><span data-ttu-id="27aff-119"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="27aff-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="27aff-120">Die Anzahl von Bytes, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="27aff-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="27aff-121"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="27aff-121"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="27aff-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27aff-122">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="27aff-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="27aff-123">Return value</span></span>
>>>>>>> <span data-ttu-id="27aff-124">master</span><span class="sxs-lookup"><span data-stu-id="27aff-124">master</span></span>

<span data-ttu-id="27aff-125">Variant</span><span class="sxs-lookup"><span data-stu-id="27aff-125">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="27aff-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="27aff-126">Remarks</span></span>

<span data-ttu-id="27aff-p101">Die durch GetChunk zurückgegebenen Bytes werden Variable zugewiesen. Mithilfe von GetChunk geben Sie jeweils einen Teil des gesamten Datenwerts zurück. Sie können die AppendChunk-Methode verwenden, um die Teile wieder zusammenzufügen.</span><span class="sxs-lookup"><span data-stu-id="27aff-p101">The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="27aff-130">Wenn offset gleich 0 ist, beginnt GetChunk ab dem ersten Byte des Felds mit dem Kopieren.</span><span class="sxs-lookup"><span data-stu-id="27aff-130">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="27aff-131">Wenn Numbytes größer als die Anzahl von Bytes im Feld ist, gibt **GetChunk** die tatsächliche Anzahl von verbliebenen Bytes im Feld zurück.</span><span class="sxs-lookup"><span data-stu-id="27aff-131">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>


> [!NOTE]
> <span data-ttu-id="27aff-p102">[!HINWEIS] Verwenden Sie ein **Memo**-Feld für Text, und schreiben Sie binäre Daten nur in Felder des Typs **Long Binary**. Andernfalls erzielen Sie unerwünschte Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="27aff-p102">Use a **Memo** field for text, and put binary data only in **Long Binary** fields. Doing otherwise will cause undesirable results.</span></span>



## <a name="example"></a><span data-ttu-id="27aff-134">Beispiel</span><span class="sxs-lookup"><span data-stu-id="27aff-134">Example</span></span>

<span data-ttu-id="27aff-p103">In diesem Beispiel werden die Methoden **AppendChunk** und **GetChunk** verwendet, um ein OLE-Objektfeld mit Daten aus einem anderen Datensatz zu füllen (immer jeweils 32 KB). In einer echten Anwendung kann es sinnvoll sein, mit einer Prozedur wie dieser einen Mitarbeiterdatensatz (inklusive Foto des Mitarbeiters) von einer Tabelle in eine andere zu kopieren. In diesem Beispiel wird der Datensatz einfach wieder in dieselbe Tabelle kopiert. Beachten Sie, dass die gesamte Bearbeitung des Abschnitts innerhalb einer einzelnen AddNew-Aktualisierungssequenz erfolgt.</span><span class="sxs-lookup"><span data-stu-id="27aff-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

```vb
    Sub AppendChunkX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstEmployees2 As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     ' Open two recordsets from the Employees table. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Set rstEmployees2 = rstEmployees.Clone 
     
     ' Add a new record to the first Recordset and copy the 
     ' data from a record in the second Recordset. 
     With rstEmployees 
     .AddNew 
     !FirstName = rstEmployees2!FirstName 
     !LastName = rstEmployees2!LastName 
     CopyLargeField rstEmployees2!Photo, !Photo 
     .Update 
     
     ' Delete new record because this is a demonstration. 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     rstEmployees2.Close 
     dbsNorthwind.Close 
     
    End Sub 
     
    Function CopyLargeField(fldSource As Field, _ 
     fldDestination As Field) 
     
     ' Set size of chunk in bytes. 
     Const conChunkSize = 32768 
     
     Dim lngOffset As Long 
     Dim lngTotalSize As Long 
     Dim strChunk As String 
     
     ' Copy the photo from one Recordset to the other in 32K 
     ' chunks until the entire field is copied. 
     lngTotalSize = fldSource.FieldSize 
     Do While lngOffset < lngTotalSize 
     strChunk = fldSource.GetChunk(lngOffset, conChunkSize) 
     fldDestination.AppendChunk strChunk 
     lngOffset = lngOffset + conChunkSize 
     Loop 
     
    End Function
```
