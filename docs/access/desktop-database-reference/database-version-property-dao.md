---
title: Database.Version-Eigenschaft (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 611fed16c9020b0a6499427af0788bf9ff050c28
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25936560"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="64d6a-102">Database.Version-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="64d6a-102">Database.Version property (DAO)</span></span>

<span data-ttu-id="64d6a-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="64d6a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="64d6a-p101">In einem Microsoft Access-Arbeitsbereich gibt diese Eigenschaft die Version der Microsoft Jet- oder Microsoft Access-Datenbank-Engine zurück, mit der die Datenbank erstellt wurde. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="64d6a-p101">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="64d6a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="64d6a-106">Syntax</span></span>

<span data-ttu-id="64d6a-107">*Ausdruck* . Version</span><span class="sxs-lookup"><span data-stu-id="64d6a-107">*expression* .Version</span></span>

<span data-ttu-id="64d6a-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="64d6a-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="64d6a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="64d6a-109">Remarks</span></span>

<span data-ttu-id="64d6a-110">Der Rückgabewert ist ein String-Datentyp, der als Versionsnummer im folgenden Format ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="64d6a-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

- <span data-ttu-id="64d6a-p102">Der Microsoft Access-Arbeitsbereich stellt die Versionsnummer in der Form major.minor dar, z. B. 3.0. Die Produktversionsnummer besteht aus der Versionsnummer (3), einem Punkt und einer Releasenummer (0).</span><span class="sxs-lookup"><span data-stu-id="64d6a-p102">Microsoft Access workspace represents the version number in the form "*major.minor*". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="64d6a-114">Die folgende Tabelle zeigt, welche Version der Datenbank-Engine in verschiedenen Versionen von Microsoft-Produkten enthalten waren.</span><span class="sxs-lookup"><span data-stu-id="64d6a-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="64d6a-115">Datenbank-Engine</span><span class="sxs-lookup"><span data-stu-id="64d6a-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="64d6a-116">Version (Freigabejahr)</span><span class="sxs-lookup"><span data-stu-id="64d6a-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="64d6a-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="64d6a-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="64d6a-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="64d6a-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="64d6a-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="64d6a-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="64d6a-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="64d6a-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64d6a-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="64d6a-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="64d6a-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="64d6a-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-123">1,0</span><span class="sxs-lookup"><span data-stu-id="64d6a-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="64d6a-124">n/v</span><span class="sxs-lookup"><span data-stu-id="64d6a-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="64d6a-125">–</span><span class="sxs-lookup"><span data-stu-id="64d6a-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="64d6a-126">n/v</span><span class="sxs-lookup"><span data-stu-id="64d6a-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64d6a-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="64d6a-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="64d6a-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="64d6a-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-129">1.1</span><span class="sxs-lookup"><span data-stu-id="64d6a-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="64d6a-130">3.0</span><span class="sxs-lookup"><span data-stu-id="64d6a-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="64d6a-131">n/v</span><span class="sxs-lookup"><span data-stu-id="64d6a-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="64d6a-132">n/v</span><span class="sxs-lookup"><span data-stu-id="64d6a-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64d6a-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="64d6a-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="64d6a-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="64d6a-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-135">2.0</span><span class="sxs-lookup"><span data-stu-id="64d6a-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="64d6a-136">n/v</span><span class="sxs-lookup"><span data-stu-id="64d6a-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="64d6a-137">–</span><span class="sxs-lookup"><span data-stu-id="64d6a-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="64d6a-138">n/v</span><span class="sxs-lookup"><span data-stu-id="64d6a-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64d6a-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="64d6a-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="64d6a-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="64d6a-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-141">n/v</span><span class="sxs-lookup"><span data-stu-id="64d6a-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="64d6a-142">4.0 (16-Bit)</span><span class="sxs-lookup"><span data-stu-id="64d6a-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-143">n/v</span><span class="sxs-lookup"><span data-stu-id="64d6a-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="64d6a-144">n/v</span><span class="sxs-lookup"><span data-stu-id="64d6a-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64d6a-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="64d6a-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="64d6a-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="64d6a-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-147">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="64d6a-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-148">4.0 (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="64d6a-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-149">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="64d6a-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-150">4.x</span><span class="sxs-lookup"><span data-stu-id="64d6a-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64d6a-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="64d6a-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="64d6a-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="64d6a-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-153">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="64d6a-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-154">5.0</span><span class="sxs-lookup"><span data-stu-id="64d6a-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="64d6a-155">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="64d6a-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-156">5.0</span><span class="sxs-lookup"><span data-stu-id="64d6a-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64d6a-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="64d6a-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="64d6a-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="64d6a-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="64d6a-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="64d6a-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="64d6a-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64d6a-161">Microsoft Access-Datenbank-Engine</span><span class="sxs-lookup"><span data-stu-id="64d6a-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="64d6a-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="64d6a-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="64d6a-163">2007</span><span class="sxs-lookup"><span data-stu-id="64d6a-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

