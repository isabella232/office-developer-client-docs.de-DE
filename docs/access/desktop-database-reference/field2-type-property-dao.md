---
title: Field2.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e1ebb10e2a9248ec38d49a874cf319c3120cd009
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877002"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="c2a41-102">Field2.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="c2a41-102">Field2.Type Property (DAO)</span></span>


<span data-ttu-id="c2a41-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c2a41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c2a41-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff **Integer**.</span><span class="sxs-lookup"><span data-stu-id="c2a41-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2a41-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2a41-106">Syntax</span></span>

<span data-ttu-id="c2a41-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="c2a41-107">*expression* .Type</span></span>

<span data-ttu-id="c2a41-108">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="c2a41-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2a41-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2a41-109">Remarks</span></span>

<span data-ttu-id="c2a41-p102">Die Einstellung oder der Rückgabewert ist eine Konstante, die den Funktions- oder Datentyp angibt. Bei einem **Field2**-Objekt besteht für diese Eigenschaft Lese-/Schreibzugriff, bis das Objekt einer Auflistung oder einem andern Objekt angefügt wird. Dann ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="c2a41-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="c2a41-112">Die möglichen Einstellungen und Rückgabewerte bei einem **Field2**-Objekt werden in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2a41-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c2a41-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="c2a41-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="c2a41-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2a41-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-116">Große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="c2a41-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-118">Binär</span><span class="sxs-lookup"><span data-stu-id="c2a41-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-120">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="c2a41-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-122">Byte</span><span class="sxs-lookup"><span data-stu-id="c2a41-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-124">Zeichen</span><span class="sxs-lookup"><span data-stu-id="c2a41-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-126">Währung</span><span class="sxs-lookup"><span data-stu-id="c2a41-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-128">Datum/Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="c2a41-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-130">Dezimal</span><span class="sxs-lookup"><span data-stu-id="c2a41-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-132">Double</span><span class="sxs-lookup"><span data-stu-id="c2a41-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-134">Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="c2a41-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-136">GUID</span><span class="sxs-lookup"><span data-stu-id="c2a41-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-138">Integer</span><span class="sxs-lookup"><span data-stu-id="c2a41-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-140">Long</span><span class="sxs-lookup"><span data-stu-id="c2a41-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-142">Langer Binärwert (OLE-Objekt)</span><span class="sxs-lookup"><span data-stu-id="c2a41-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-143"><strong>Wert dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-144">Memo</span><span class="sxs-lookup"><span data-stu-id="c2a41-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-146">Numerisch</span><span class="sxs-lookup"><span data-stu-id="c2a41-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-148">Single</span><span class="sxs-lookup"><span data-stu-id="c2a41-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-150">Text</span><span class="sxs-lookup"><span data-stu-id="c2a41-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-151"><strong>Zeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-152">Zeit</span><span class="sxs-lookup"><span data-stu-id="c2a41-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c2a41-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-154">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="c2a41-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c2a41-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="c2a41-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="c2a41-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="c2a41-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c2a41-157">Beim Anfügen eines neuen **Field2**-, **Parameter**- oder **Property**-Objekts zur Auflistung eines **Index**-, **QueryDef**-, **Recordset**- oder **TableDef**-Objekts tritt ein Fehler auf, wenn die zugrunde liegende Tabelle den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2a41-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

