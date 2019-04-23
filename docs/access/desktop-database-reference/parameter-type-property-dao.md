---
title: Parameter. Type-Eigenschaft (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 208d0a5097b8473fef60b94f972f2c8579150fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288021"
---
# <a name="parametertype-property-dao"></a><span data-ttu-id="9381e-102">Parameter. Type-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="9381e-102">Parameter.Type property (DAO)</span></span>


<span data-ttu-id="9381e-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9381e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9381e-104">Legt einen Wert fest, der den Funktions- oder Datentyp eines Objekts angibt, oder gibt diesen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9381e-104">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="9381e-105">**Integer**-Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="9381e-105">Read/write **Integer**.</span></span>

## <a name="syntax"></a><span data-ttu-id="9381e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9381e-106">Syntax</span></span>

<span data-ttu-id="9381e-107">*Ausdruck* . Typ</span><span class="sxs-lookup"><span data-stu-id="9381e-107">*expression* .Type</span></span>

<span data-ttu-id="9381e-108">*Ausdruck* Eine Variable, die ein **Parameter** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="9381e-108">*expression* A variable that represents a **Parameter** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="9381e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9381e-109">Remarks</span></span>

<span data-ttu-id="9381e-p102">Die Einstellung bzw. der Rückgabewert ist eine Konstante, die einen Funktions- oder Datentyp angibt. Für ein **[Parameter](parameter-object-dao.md)** -Objekt in einem Microsoft Access-Arbeitsbereich ist die Eigenschaft schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9381e-p102">The setting or return value is a constant that indicates an operational or data type. For a **[Parameter](parameter-object-dao.md)** object in a Microsoft Access workspace the property is read-only.</span></span>

<span data-ttu-id="9381e-112">Die möglichen Einstellungen und Rückgabewerte für ein **Parameter**-Objekt sind in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9381e-112">For a **Parameter** object, the possible settings and return values are described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="9381e-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="9381e-113">Constant</span></span></p></th>
<th><p><span data-ttu-id="9381e-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9381e-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9381e-115"><strong>dbBigint</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-115"><strong>dbBigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-116">Große Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="9381e-116">Big Integer</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-117"><strong>dbBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-117"><strong>dbBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-118">Binär</span><span class="sxs-lookup"><span data-stu-id="9381e-118">Binary</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-119"><strong>dbBoolean</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-119"><strong>dbBoolean</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-120">Boolescher Wert</span><span class="sxs-lookup"><span data-stu-id="9381e-120">Boolean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-121"><strong>dbByte</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-121"><strong>dbByte</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-122">Byte</span><span class="sxs-lookup"><span data-stu-id="9381e-122">Byte</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-123"><strong>dbChar</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-123"><strong>dbChar</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-124">Zeichen</span><span class="sxs-lookup"><span data-stu-id="9381e-124">Char</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-125"><strong>dbCurrency</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-125"><strong>dbCurrency</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-126">Währung</span><span class="sxs-lookup"><span data-stu-id="9381e-126">Currency</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-127"><strong>dbDate</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-127"><strong>dbDate</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-128">Datum/Uhrzeit</span><span class="sxs-lookup"><span data-stu-id="9381e-128">Date/Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-129"><strong>dbDecimal</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-129"><strong>dbDecimal</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-130">Dezimal</span><span class="sxs-lookup"><span data-stu-id="9381e-130">Decimal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-131"><strong>dbDouble</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-131"><strong>dbDouble</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-132">Double</span><span class="sxs-lookup"><span data-stu-id="9381e-132">Double</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-133"><strong>dbFloat</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-133"><strong>dbFloat</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-134">Gleitkomma</span><span class="sxs-lookup"><span data-stu-id="9381e-134">Float</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-135"><strong>dbGUID</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-135"><strong>dbGUID</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-136">GUID</span><span class="sxs-lookup"><span data-stu-id="9381e-136">GUID</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-137"><strong>dbInteger</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-137"><strong>dbInteger</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-138">Integer</span><span class="sxs-lookup"><span data-stu-id="9381e-138">Integer</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-139"><strong>dbLong</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-139"><strong>dbLong</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-140">Long</span><span class="sxs-lookup"><span data-stu-id="9381e-140">Long</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-141"><strong>dbLongBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-141"><strong>dbLongBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-142">Langer Binärwert (OLE-Objekt)</span><span class="sxs-lookup"><span data-stu-id="9381e-142">Long Binary (OLE Object)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-143"><strong>dbMemo</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-143"><strong>dbMemo</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-144">Memo</span><span class="sxs-lookup"><span data-stu-id="9381e-144">Memo</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-145"><strong>dbNumeric</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-145"><strong>dbNumeric</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-146">Numerisch</span><span class="sxs-lookup"><span data-stu-id="9381e-146">Numeric</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-147"><strong>dbSingle</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-147"><strong>dbSingle</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-148">Single</span><span class="sxs-lookup"><span data-stu-id="9381e-148">Single</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-149"><strong>dbText</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-149"><strong>dbText</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-150">Text</span><span class="sxs-lookup"><span data-stu-id="9381e-150">Text</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-151"><strong>DBZeit</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-151"><strong>dbTime</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-152">Zeit</span><span class="sxs-lookup"><span data-stu-id="9381e-152">Time</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9381e-153"><strong>dbTimeStamp</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-153"><strong>dbTimeStamp</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-154">Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="9381e-154">Time Stamp</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9381e-155"><strong>dbVarBinary</strong></span><span class="sxs-lookup"><span data-stu-id="9381e-155"><strong>dbVarBinary</strong></span></span></p></td>
<td><p><span data-ttu-id="9381e-156">VarBinary</span><span class="sxs-lookup"><span data-stu-id="9381e-156">VarBinary</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9381e-157">Wenn Sie ein neues **Field** -, **Parameter** - oder **Property** -Objekt an die Auflistung eines **[Index](index-object-dao.md)** -, **QueryDef** -, **Recordset** - oder **TableDef** -Objekts anfügen, tritt ein Fehler auf, falls die zugrunde liegende Datenbank den für das neue Objekt angegebenen Datentyp nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9381e-157">When you append a new **Field**, **Parameter**, or **Property** object to the collection of an **[Index](index-object-dao.md)**, **QueryDef**, **Recordset**, or **TableDef** object, an error occurs if the underlying database doesn't support the data type specified for the new object.</span></span>

