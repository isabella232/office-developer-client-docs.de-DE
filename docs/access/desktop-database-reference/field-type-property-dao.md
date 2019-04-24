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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292951"
---
# <a name="fieldtype-property-dao"></a><span data-ttu-id="f559b-102">Field.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="f559b-102">Field.Type Property (DAO)</span></span>


<span data-ttu-id="f559b-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f559b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f559b-104">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f559b-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="f559b-105">**Ganze Zahl** mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="f559b-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f559b-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f559b-106">Syntax</span></span>

<span data-ttu-id="f559b-107">*expression* .Type</span><span class="sxs-lookup"><span data-stu-id="f559b-107">expression  . Type</span></span>

<span data-ttu-id="f559b-108">*Ausdruck* Eine Variable, die ein **Field**-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="f559b-108">*expression*  A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="f559b-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f559b-109">Remarks</span></span>

<span data-ttu-id="f559b-p102">Der Einstellungs- oder Rückgabewert ist eine Konstante, die einen Funktions- oder Datentyp angibt. Für ein **Field** -Objekt besteht für diese Eigenschaft Lese-/Schreibzugriff, bis das Objekt an eine Auflistung oder ein anderes Objekt angefügt wird; anschließend ist sie schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="f559b-p102">The setting or return value is a constant that indicates an operational or data type. For a **Field** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="f559b-112">Die möglichen Einstellungs- und Rückgabewerte für ein **Field** -Objekt werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f559b-112">For a **Field** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f559b-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="f559b-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="f559b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f559b-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f559b-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-116">Große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="f559b-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-118">Binär</span><span class="sxs-lookup"><span data-stu-id="f559b-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-120">Boolesch</span><span class="sxs-lookup"><span data-stu-id="f559b-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-122">Byte</span><span class="sxs-lookup"><span data-stu-id="f559b-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-124">Char</span><span class="sxs-lookup"><span data-stu-id="f559b-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-126">Währung</span><span class="sxs-lookup"><span data-stu-id="f559b-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-128">Datum/Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="f559b-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-130">Decimal</span><span class="sxs-lookup"><span data-stu-id="f559b-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-132">Gleitkommawert mit doppelter Genauigkeit</span><span class="sxs-lookup"><span data-stu-id="f559b-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-134">Gleitkommazahl</span><span class="sxs-lookup"><span data-stu-id="f559b-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-136">GUID</span><span class="sxs-lookup"><span data-stu-id="f559b-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-138">Ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="f559b-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-140">Long</span><span class="sxs-lookup"><span data-stu-id="f559b-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-142">Langer Binärwert (OLE-Objekt)</span><span class="sxs-lookup"><span data-stu-id="f559b-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-144">Memo</span><span class="sxs-lookup"><span data-stu-id="f559b-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-146">Numeric</span><span class="sxs-lookup"><span data-stu-id="f559b-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-148">Single</span><span class="sxs-lookup"><span data-stu-id="f559b-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-150">Text</span><span class="sxs-lookup"><span data-stu-id="f559b-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-151"><strong>dbTime</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-152">Time</span><span class="sxs-lookup"><span data-stu-id="f559b-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f559b-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-154">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="f559b-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f559b-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="f559b-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="f559b-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="f559b-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="f559b-157">Wenn Sie ein neues **Field** -, **Parameter** - oder **Property** -Objekt an die Auflistung eines **[Index](index-object-dao.md)** -, **QueryDef** -, **Recordset** - oder **TableDef** -Objekts anfügen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f559b-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

