---
title: Property.Type Property (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 15a1ac18a504a723948b8f1539c1bf002cf9833a
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25888146"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="1983f-102">Property.Type Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="1983f-102">Property.Type Property (DAO)</span></span>


<span data-ttu-id="1983f-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1983f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1983f-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff **Integer**.</span><span class="sxs-lookup"><span data-stu-id="1983f-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1983f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1983f-106">Syntax</span></span>

<span data-ttu-id="1983f-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="1983f-107">*expression* .Type</span></span>

<span data-ttu-id="1983f-108">*Ausdruck* Eine Variable, die ein **Property-** Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="1983f-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1983f-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1983f-109">Remarks</span></span>

<span data-ttu-id="1983f-p102">Die Einstellung bzw. der Rückgabewert ist eine Konstante, die einen Funktions- oder Datentyp angibt. Ein **[Property](property-object-dao.md)** -Objekt hat Lese-/Schreibzugriff für diese Eigenschaft. Wenn das Objekt an eine Auflistung oder ein anderes Objekt angehängt wird, ist die Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="1983f-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="1983f-112">Die möglichen Einstellungen und Rückgabewerte für ein **Property**-Objekt sind in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1983f-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1983f-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="1983f-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="1983f-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1983f-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1983f-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-116">Große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="1983f-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-118">Binär</span><span class="sxs-lookup"><span data-stu-id="1983f-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-120">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="1983f-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-122">Byte</span><span class="sxs-lookup"><span data-stu-id="1983f-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-124">Zeichen</span><span class="sxs-lookup"><span data-stu-id="1983f-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-126">Währung</span><span class="sxs-lookup"><span data-stu-id="1983f-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-128">Datum/Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="1983f-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-130">Dezimal</span><span class="sxs-lookup"><span data-stu-id="1983f-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-132">Double</span><span class="sxs-lookup"><span data-stu-id="1983f-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-134">Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="1983f-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-136">GUID</span><span class="sxs-lookup"><span data-stu-id="1983f-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-138">Integer</span><span class="sxs-lookup"><span data-stu-id="1983f-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-140">Long</span><span class="sxs-lookup"><span data-stu-id="1983f-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-142">Langer Binärwert (OLE-Objekt)</span><span class="sxs-lookup"><span data-stu-id="1983f-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-143"><strong>Wert dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-144">Memo</span><span class="sxs-lookup"><span data-stu-id="1983f-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-146">Numerisch</span><span class="sxs-lookup"><span data-stu-id="1983f-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-148">Single</span><span class="sxs-lookup"><span data-stu-id="1983f-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-150">Text</span><span class="sxs-lookup"><span data-stu-id="1983f-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-151"><strong>Zeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-152">Zeit</span><span class="sxs-lookup"><span data-stu-id="1983f-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1983f-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-154">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="1983f-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1983f-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="1983f-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="1983f-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="1983f-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1983f-157">Wenn Sie ein neues **Field** -, **Parameter** - oder **Property** -Objekt an die Auflistung eines **[Index](index-object-dao.md)** -, **QueryDef** -, **Recordset** - oder **TableDef** -Objekts anfügen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1983f-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

