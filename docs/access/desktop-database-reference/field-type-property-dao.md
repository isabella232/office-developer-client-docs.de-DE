---
title: Field.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 37891aa3ee9c6329e1295b730b4f72779d16e0a3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/31/2018
ms.locfileid: "25875392"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="91f1b-102">Field.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="91f1b-102">Field.Type Property (DAO)</span></span>


<span data-ttu-id="91f1b-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="91f1b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="91f1b-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff **Integer**.</span><span class="sxs-lookup"><span data-stu-id="91f1b-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="91f1b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="91f1b-106">Syntax</span></span>

<span data-ttu-id="91f1b-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="91f1b-107">*expression* .Type</span></span>

<span data-ttu-id="91f1b-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="91f1b-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="91f1b-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="91f1b-109">Remarks</span></span>

<span data-ttu-id="91f1b-p102">Der Einstellungs- oder Rückgabewert ist eine Konstante, die einen Funktions- oder Datentyp angibt. Für ein **Field** -Objekt besteht für diese Eigenschaft Lese-/Schreibzugriff, bis das Objekt an eine Auflistung oder ein anderes Objekt angefügt wird; anschließend ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="91f1b-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="91f1b-112">Die möglichen Einstellungs- und Rückgabewerte für ein **Field** -Objekt werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="91f1b-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="91f1b-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="91f1b-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="91f1b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="91f1b-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-116">Große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="91f1b-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-118">Binär</span><span class="sxs-lookup"><span data-stu-id="91f1b-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-120">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="91f1b-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-122">Byte</span><span class="sxs-lookup"><span data-stu-id="91f1b-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-124">Zeichen</span><span class="sxs-lookup"><span data-stu-id="91f1b-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-126">Währung</span><span class="sxs-lookup"><span data-stu-id="91f1b-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-128">Datum/Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="91f1b-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-130">Dezimal</span><span class="sxs-lookup"><span data-stu-id="91f1b-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-132">Double</span><span class="sxs-lookup"><span data-stu-id="91f1b-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-134">Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="91f1b-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-136">GUID</span><span class="sxs-lookup"><span data-stu-id="91f1b-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-138">Integer</span><span class="sxs-lookup"><span data-stu-id="91f1b-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-140">Long</span><span class="sxs-lookup"><span data-stu-id="91f1b-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-142">Langer Binärwert (OLE-Objekt)</span><span class="sxs-lookup"><span data-stu-id="91f1b-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-143"><strong>Wert dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-144">Memo</span><span class="sxs-lookup"><span data-stu-id="91f1b-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-146">Numerisch</span><span class="sxs-lookup"><span data-stu-id="91f1b-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-148">Single</span><span class="sxs-lookup"><span data-stu-id="91f1b-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-150">Text</span><span class="sxs-lookup"><span data-stu-id="91f1b-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-151"><strong>Zeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-152">Zeit</span><span class="sxs-lookup"><span data-stu-id="91f1b-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91f1b-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-154">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="91f1b-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91f1b-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="91f1b-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="91f1b-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="91f1b-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91f1b-157">Wenn Sie ein neues **Field** -, **Parameter** - oder **Property** -Objekt an die Auflistung eines **[Index](index-object-dao.md)** -, **QueryDef** -, **Recordset** - oder **TableDef** -Objekts anfügen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91f1b-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

