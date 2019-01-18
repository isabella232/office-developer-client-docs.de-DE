---
title: Field2.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 057d6ec9-b72c-cee6-005a-6d916e3dda29
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844921(v=office.15)
ms:contentKeyID: 48543032
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4da32f18a2b3e9dddbb0ae04e3257de34ba09761
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699786"
---
# <a name="field2type-property-dao"></a><span data-ttu-id="14d87-102">Field2.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="14d87-102">Field2.Type property (DAO)</span></span>


<span data-ttu-id="14d87-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="14d87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="14d87-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff **Integer**.</span><span class="sxs-lookup"><span data-stu-id="14d87-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="14d87-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="14d87-106">Syntax</span></span>

<span data-ttu-id="14d87-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="14d87-107">*expression* .Type</span></span>

<span data-ttu-id="14d87-108">*Ausdruck* Eine Variable, die ein **Field2** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="14d87-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="14d87-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14d87-109">Remarks</span></span>

<span data-ttu-id="14d87-p102">Die Einstellung oder der Rückgabewert ist eine Konstante, die den Funktions- oder Datentyp angibt. Bei einem **Field2**-Objekt besteht für diese Eigenschaft Lese-/Schreibzugriff, bis das Objekt einer Auflistung oder einem andern Objekt angefügt wird. Dann ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="14d87-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field2** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="14d87-112">Die möglichen Einstellungen und Rückgabewerte bei einem **Field2**-Objekt werden in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="14d87-112">For a **Field2** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="14d87-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="14d87-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="14d87-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14d87-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14d87-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-116">Große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="14d87-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-118">Binär</span><span class="sxs-lookup"><span data-stu-id="14d87-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-120">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="14d87-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-122">Byte</span><span class="sxs-lookup"><span data-stu-id="14d87-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-124">Zeichen</span><span class="sxs-lookup"><span data-stu-id="14d87-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-126">Währung</span><span class="sxs-lookup"><span data-stu-id="14d87-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-128">Datum/Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="14d87-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-130">Dezimal</span><span class="sxs-lookup"><span data-stu-id="14d87-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-132">Double</span><span class="sxs-lookup"><span data-stu-id="14d87-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-134">Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="14d87-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-136">GUID</span><span class="sxs-lookup"><span data-stu-id="14d87-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-138">Integer</span><span class="sxs-lookup"><span data-stu-id="14d87-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-140">Long</span><span class="sxs-lookup"><span data-stu-id="14d87-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-142">Langer Binärwert (OLE-Objekt)</span><span class="sxs-lookup"><span data-stu-id="14d87-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-143"><strong>Wert dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-144">Memo</span><span class="sxs-lookup"><span data-stu-id="14d87-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-146">Numerisch</span><span class="sxs-lookup"><span data-stu-id="14d87-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-148">Single</span><span class="sxs-lookup"><span data-stu-id="14d87-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-150">Text</span><span class="sxs-lookup"><span data-stu-id="14d87-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-151"><strong>Zeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-152">Zeit</span><span class="sxs-lookup"><span data-stu-id="14d87-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d87-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-154">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="14d87-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d87-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="14d87-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="14d87-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="14d87-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="14d87-157">Beim Anfügen eines neuen **Field2**-, **Parameter**- oder **Property**-Objekts zur Auflistung eines **Index**-, **QueryDef**-, **Recordset**- oder **TableDef**-Objekts tritt ein Fehler auf, wenn die zugrunde liegende Tabelle den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="14d87-157">When you append a new **Field2**, **Parameter**, or **Property** object to the collection of an **Index**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

