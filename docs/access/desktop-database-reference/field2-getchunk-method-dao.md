---
title: Field2.GetChunk-Methode (DAO)
TOCTitle: GetChunk method
ms:assetid: 5d3a66c0-8216-d701-0a91-b79fbbc822b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194600(v=office.15)
ms:contentKeyID: 48545101
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fae8e5f0331f3c59aad482b827140ecd6366f2f1
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/06/2018
ms.locfileid: "25996433"
---
# <a name="field2getchunk-method-dao"></a><span data-ttu-id="e1af4-102">Field2.GetChunk-Methode (DAO)</span><span class="sxs-lookup"><span data-stu-id="e1af4-102">Field2.GetChunk method (DAO)</span></span>

<span data-ttu-id="e1af4-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e1af4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e1af4-104">Gibt den gesamten oder einen Teil des Inhalts eines Objekts **vom Typ Memo** oder **Long Field2** in der **[Fields](fields-collection-dao.md)** -Auflistung eines **[Recordset](recordset-object-dao.md)** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="e1af4-104">Returns all or a portion of the contents of a **Memo** or **Long BinaryField2** object in the **[Fields](fields-collection-dao.md)** collection of a **[Recordset](recordset-object-dao.md)** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1af4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1af4-105">Syntax</span></span>

<span data-ttu-id="e1af4-106">*Ausdruck* . GetChunk (***Offset***, ***Byte***)</span><span class="sxs-lookup"><span data-stu-id="e1af4-106">*expression* .GetChunk(***Offset***, ***Bytes***)</span></span>

<span data-ttu-id="e1af4-107">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e1af4-107">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e1af4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1af4-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e1af4-109">Name</span><span class="sxs-lookup"><span data-stu-id="e1af4-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e1af4-110">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="e1af4-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e1af4-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e1af4-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="e1af4-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1af4-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e1af4-113"><em>Offset</em></span><span class="sxs-lookup"><span data-stu-id="e1af4-113"><em>Offset</em></span></span></p></td>
<td><p><span data-ttu-id="e1af4-114">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e1af4-114">Required</span></span></p></td>
<td><p><span data-ttu-id="e1af4-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="e1af4-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="e1af4-116">Die Anzahl von zu überspringenden Bytes, bevor das Kopieren gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e1af4-116">The number of bytes to skip before copying begins.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e1af4-117"><em>Bytes</em></span><span class="sxs-lookup"><span data-stu-id="e1af4-117"><em>Bytes</em></span></span></p></td>
<td><p><span data-ttu-id="e1af4-118">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="e1af4-118">Required</span></span></p></td>
<td><p><span data-ttu-id="e1af4-119"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="e1af4-119"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="e1af4-120">Die Anzahl von Bytes, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e1af4-120">The number of bytes you want to return.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="e1af4-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e1af4-121">Return value</span></span>

<span data-ttu-id="e1af4-122">Variant</span><span class="sxs-lookup"><span data-stu-id="e1af4-122">Variant</span></span>

## <a name="remarks"></a><span data-ttu-id="e1af4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1af4-123">Remarks</span></span>

<span data-ttu-id="e1af4-p101">Die durch GetChunk zurückgegebenen Bytes werden Variable zugewiesen. Mithilfe von GetChunk geben Sie jeweils einen Teil des gesamten Datenwerts zurück. Sie können die AppendChunk-Methode verwenden, um die Teile wieder zusammenzufügen.</span><span class="sxs-lookup"><span data-stu-id="e1af4-p101">The bytes returned by **GetChunk** are assigned to variable. Use **GetChunk** to return a portion of the total data value at a time. You can use the **[AppendChunk](field-appendchunk-method-dao.md)** method to reassemble the pieces.</span></span>

<span data-ttu-id="e1af4-127">Wenn offset gleich 0 ist, beginnt GetChunk ab dem ersten Byte des Felds mit dem Kopieren.</span><span class="sxs-lookup"><span data-stu-id="e1af4-127">If offset is 0, **GetChunk** begins copying from the first byte of the field.</span></span>

<span data-ttu-id="e1af4-128">Wenn Numbytes größer als die Anzahl von Bytes im Feld ist, gibt **GetChunk** die tatsächliche Anzahl von verbliebenen Bytes im Feld zurück.</span><span class="sxs-lookup"><span data-stu-id="e1af4-128">If numbytes is greater than the number of bytes in the field, **GetChunk** returns the actual number of remaining bytes in the field.</span></span>

> [!NOTE]
> <span data-ttu-id="e1af4-p102">[!HINWEIS] Verwenden Sie ein **Memo**-Feld für Text, und schreiben Sie binäre Daten nur in Felder des Typs **Long Binary**. Andernfalls erzielen Sie unerwünschte Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="e1af4-p102">Use a **Memo** field for text, and put binary data only in **Long Binary** fields. Doing otherwise will cause undesirable results.</span></span>

## <a name="example"></a><span data-ttu-id="e1af4-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e1af4-131">Example</span></span>

<span data-ttu-id="e1af4-p103">In diesem Beispiel werden die Methoden **AppendChunk** und **GetChunk** verwendet, um ein OLE-Objektfeld mit Daten aus einem anderen Datensatz zu füllen (immer jeweils 32 KB). In einer echten Anwendung kann es sinnvoll sein, mit einer Prozedur wie dieser einen Mitarbeiterdatensatz (inklusive Foto des Mitarbeiters) von einer Tabelle in eine andere zu kopieren. In diesem Beispiel wird der Datensatz einfach wieder in dieselbe Tabelle kopiert. Beachten Sie, dass die gesamte Bearbeitung des Abschnitts innerhalb einer einzelnen AddNew-Aktualisierungssequenz erfolgt.</span><span class="sxs-lookup"><span data-stu-id="e1af4-p103">This example uses the **AppendChunk** and **GetChunk** methods to fill an OLE object field with data from another record, 32K at a time. In a real application, one might use a procedure like this to copy an employee record (including the employee's photo) from one table to another. In this example, the record is simply being copied back to same table. Note that all the chunk manipulation takes place within a single AddNew-Update sequence.</span></span>

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
     
    Function CopyLargeField(fldSource As Field2, _ 
     fldDestination As Field2) 
     
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
