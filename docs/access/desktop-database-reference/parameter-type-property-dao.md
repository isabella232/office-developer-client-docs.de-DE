---
title: Parameter.Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 294d61ba964958d7933a68919df940cb7501ec0d
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25927032"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="6e759-102">Parameter.Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="6e759-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="6e759-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e759-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6e759-p101">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt einen solchen Wert zurück. Lese-/Schreibzugriff **Integer**.</span><span class="sxs-lookup"><span data-stu-id="6e759-p101">Sets or returns a value that indicates the operational type or data type of an object. Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e759-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e759-106">Syntax</span></span>

<span data-ttu-id="6e759-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="6e759-107">*expression* .Type</span></span>

<span data-ttu-id="6e759-108">*Ausdruck* Eine Variable, die ein **Parameter** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="6e759-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e759-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e759-109">Remarks</span></span>

<span data-ttu-id="6e759-p102">Die Einstellung bzw. der Rückgabewert ist eine Konstante, die einen Funktions- oder Datentyp angibt. Für ein **[Parameter](parameter-object-dao.md)** -Objekt in einem Microsoft Access-Arbeitsbereich ist die Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6e759-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="6e759-112">Die möglichen Einstellungen und Rückgabewerte für ein **Parameter**-Objekt sind in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6e759-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6e759-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="6e759-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="6e759-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6e759-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e759-115"><strong>dbBigInt</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-116">Große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="6e759-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-118">Binär</span><span class="sxs-lookup"><span data-stu-id="6e759-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-120">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="6e759-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-122">Byte</span><span class="sxs-lookup"><span data-stu-id="6e759-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-124">Zeichen</span><span class="sxs-lookup"><span data-stu-id="6e759-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-126">Währung</span><span class="sxs-lookup"><span data-stu-id="6e759-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-128">Datum/Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="6e759-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-130">Dezimal</span><span class="sxs-lookup"><span data-stu-id="6e759-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-132">Double</span><span class="sxs-lookup"><span data-stu-id="6e759-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-134">Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="6e759-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-136">GUID</span><span class="sxs-lookup"><span data-stu-id="6e759-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-138">Integer</span><span class="sxs-lookup"><span data-stu-id="6e759-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-140">Long</span><span class="sxs-lookup"><span data-stu-id="6e759-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-142">Langer Binärwert (OLE-Objekt)</span><span class="sxs-lookup"><span data-stu-id="6e759-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-143"><strong>Wert dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-144">Memo</span><span class="sxs-lookup"><span data-stu-id="6e759-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-146">Numerisch</span><span class="sxs-lookup"><span data-stu-id="6e759-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-148">Single</span><span class="sxs-lookup"><span data-stu-id="6e759-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-150">Text</span><span class="sxs-lookup"><span data-stu-id="6e759-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-151"><strong>Zeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-152">Zeit</span><span class="sxs-lookup"><span data-stu-id="6e759-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e759-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-154">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="6e759-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e759-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="6e759-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="6e759-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="6e759-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="6e759-157">Wenn Sie ein neues **Field** -, **Parameter** - oder **Property** -Objekt an die Auflistung eines **[Index](index-object-dao.md)** -, **QueryDef** -, **Recordset** - oder **TableDef** -Objekts anfügen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6e759-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

