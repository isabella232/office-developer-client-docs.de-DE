---
title: Eigenschaft. Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4280b89102e06b2ecc09a783840e671b0af9ff73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302899"
---
# <a name="propertytype-property-dao"></a><span data-ttu-id="47510-102">Eigenschaft. Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="47510-102">Property.Type property (DAO)</span></span>


<span data-ttu-id="47510-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="47510-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="47510-104">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="47510-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="47510-105">**Integer**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="47510-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="47510-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="47510-106">Syntax</span></span>

<span data-ttu-id="47510-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="47510-107">*expression* .Type</span></span>

<span data-ttu-id="47510-108">*Ausdruck* Eine Variable, die ein **Property-** Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="47510-108">*expression* A variable that represents a **Property** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="47510-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47510-109">Remarks</span></span>

<span data-ttu-id="47510-p102">Die Einstellung bzw. der Rückgabewert ist eine Konstante, die einen Funktions- oder Datentyp angibt. Ein **[Property](property-object-dao.md)** -Objekt hat Lese-/Schreibzugriff für diese Eigenschaft. Wenn das Objekt an eine Auflistung oder ein anderes Objekt angehängt wird, ist die Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="47510-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Property](property-object-dao.md)** object, this property is read/write until the object is appended to a collection or to another object, after which it's read-only.</span></span>

<span data-ttu-id="47510-112">Die möglichen Einstellungen und Rückgabewerte für ein **Property**-Objekt sind in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="47510-112">For a **Property** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="47510-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="47510-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="47510-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="47510-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="47510-115"><strong>dbBigint</strong></span><span class="sxs-lookup"><span data-stu-id="47510-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-116">Große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="47510-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="47510-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-118">Binär</span><span class="sxs-lookup"><span data-stu-id="47510-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="47510-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-120">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="47510-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="47510-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-122">Byte</span><span class="sxs-lookup"><span data-stu-id="47510-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="47510-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-124">Zeichen</span><span class="sxs-lookup"><span data-stu-id="47510-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="47510-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-126">Währung</span><span class="sxs-lookup"><span data-stu-id="47510-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="47510-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-128">Datum/Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="47510-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="47510-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-130">Dezimal</span><span class="sxs-lookup"><span data-stu-id="47510-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="47510-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-132">Double</span><span class="sxs-lookup"><span data-stu-id="47510-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="47510-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-134">Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="47510-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="47510-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-136">GUID</span><span class="sxs-lookup"><span data-stu-id="47510-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="47510-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-138">Integer</span><span class="sxs-lookup"><span data-stu-id="47510-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="47510-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-140">Long</span><span class="sxs-lookup"><span data-stu-id="47510-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="47510-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-142">Langer Binärwert (OLE-Objekt)</span><span class="sxs-lookup"><span data-stu-id="47510-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="47510-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-144">Memo</span><span class="sxs-lookup"><span data-stu-id="47510-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="47510-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-146">Numerisch</span><span class="sxs-lookup"><span data-stu-id="47510-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="47510-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-148">Single</span><span class="sxs-lookup"><span data-stu-id="47510-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="47510-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-150">Text</span><span class="sxs-lookup"><span data-stu-id="47510-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-151"><strong>DBZeit</strong></span><span class="sxs-lookup"><span data-stu-id="47510-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-152">Zeit</span><span class="sxs-lookup"><span data-stu-id="47510-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="47510-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="47510-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-154">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="47510-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="47510-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="47510-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="47510-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="47510-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="47510-157">Wenn Sie ein neues **Field** -, **Parameter** - oder **Property** -Objekt an die Auflistung eines **[Index](index-object-dao.md)** -, **QueryDef** -, **Recordset** - oder **TableDef** -Objekts anfügen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="47510-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

