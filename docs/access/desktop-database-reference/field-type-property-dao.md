---
title: Field.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 1295ca40-78c1-bdd0-d407-e1b5be8adfd4
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845405(v=office.15)
ms:contentKeyID: 48543345
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c8f212c5e1f10f4270987c9453802575d88cebfa
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: de-DE
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709481"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="84976-102">Field.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="84976-102">Field.Type property (DAO)</span></span>


<span data-ttu-id="84976-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="84976-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="84976-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff **Integer**.</span><span class="sxs-lookup"><span data-stu-id="84976-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="84976-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="84976-106">Syntax</span></span>

<span data-ttu-id="84976-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="84976-107">*expression* .Type</span></span>

<span data-ttu-id="84976-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="84976-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="84976-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="84976-109">Remarks</span></span>

<span data-ttu-id="84976-p102">Der Einstellungs- oder Rückgabewert ist eine Konstante, die einen Funktions- oder Datentyp angibt. Für ein **Field** -Objekt besteht für diese Eigenschaft Lese-/Schreibzugriff, bis das Objekt an eine Auflistung oder ein anderes Objekt angefügt wird; anschließend ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="84976-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="84976-112">Die möglichen Einstellungs- und Rückgabewerte für ein **Field** -Objekt werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="84976-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="84976-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="84976-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="84976-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84976-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="84976-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="84976-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-116">Große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="84976-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="84976-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-118">Binär</span><span class="sxs-lookup"><span data-stu-id="84976-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="84976-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-120">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="84976-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="84976-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-122">Byte</span><span class="sxs-lookup"><span data-stu-id="84976-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="84976-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-124">Zeichen</span><span class="sxs-lookup"><span data-stu-id="84976-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="84976-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-126">Währung</span><span class="sxs-lookup"><span data-stu-id="84976-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="84976-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-128">Datum/Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="84976-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="84976-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-130">Dezimal</span><span class="sxs-lookup"><span data-stu-id="84976-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="84976-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-132">Double</span><span class="sxs-lookup"><span data-stu-id="84976-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="84976-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-134">Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="84976-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="84976-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-136">GUID</span><span class="sxs-lookup"><span data-stu-id="84976-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="84976-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-138">Integer</span><span class="sxs-lookup"><span data-stu-id="84976-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="84976-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-140">Long</span><span class="sxs-lookup"><span data-stu-id="84976-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="84976-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-142">Langer Binärwert (OLE-Objekt)</span><span class="sxs-lookup"><span data-stu-id="84976-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-143"><strong>Wert dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="84976-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-144">Memo</span><span class="sxs-lookup"><span data-stu-id="84976-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="84976-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-146">Numerisch</span><span class="sxs-lookup"><span data-stu-id="84976-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="84976-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-148">Single</span><span class="sxs-lookup"><span data-stu-id="84976-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="84976-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-150">Text</span><span class="sxs-lookup"><span data-stu-id="84976-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-151"><strong>Zeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="84976-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-152">Zeit</span><span class="sxs-lookup"><span data-stu-id="84976-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="84976-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="84976-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-154">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="84976-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="84976-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="84976-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="84976-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="84976-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="84976-157">Wenn Sie ein neues **Field** -, **Parameter** - oder **Property** -Objekt an die Auflistung eines **[Index](index-object-dao.md)** -, **QueryDef** -, **Recordset** - oder **TableDef** -Objekts anfügen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="84976-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

