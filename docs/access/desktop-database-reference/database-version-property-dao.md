---
title: Database.Version Property (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4bcb360caa71131f4892409805c7afe3ceb2dcce
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475987"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="933ff-102">Database.Version Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="933ff-102">Database.Version Property (DAO)</span></span>


<span data-ttu-id="933ff-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="933ff-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="933ff-p101">In einem Microsoft Access-Arbeitsbereich gibt diese Eigenschaft die Version der Microsoft Jet- oder Microsoft Access-Datenbank-Engine zurück, mit der die Datenbank erstellt wurde. Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="933ff-p101">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database. Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="933ff-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="933ff-106">Syntax</span></span>

<span data-ttu-id="933ff-107">*Ausdruck* . Version</span><span class="sxs-lookup"><span data-stu-id="933ff-107">*expression* .Version</span></span>

<span data-ttu-id="933ff-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="933ff-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="933ff-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="933ff-109">Remarks</span></span>

<span data-ttu-id="933ff-110">Der Rückgabewert ist ein String-Datentyp, der als Versionsnummer im folgenden Format ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="933ff-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

  - <span data-ttu-id="933ff-p102">Der Microsoft Access-Arbeitsbereich stellt die Versionsnummer in der Form major.minor dar, z. B. 3.0. Die Produktversionsnummer besteht aus der Versionsnummer (3), einem Punkt und einer Releasenummer (0).</span><span class="sxs-lookup"><span data-stu-id="933ff-p102">Microsoft Access workspace represents the version number in the form "*major.minor*". For example, "3.0". The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="933ff-114">Die folgende Tabelle zeigt, welche Version der Datenbank-Engine in verschiedenen Versionen von Microsoft-Produkten enthalten waren.</span><span class="sxs-lookup"><span data-stu-id="933ff-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

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
<th><p><span data-ttu-id="933ff-115">Datenbank-Engine</span><span class="sxs-lookup"><span data-stu-id="933ff-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="933ff-116">Version (Freigabejahr)</span><span class="sxs-lookup"><span data-stu-id="933ff-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="933ff-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="933ff-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="933ff-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="933ff-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="933ff-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="933ff-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="933ff-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="933ff-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="933ff-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933ff-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933ff-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="933ff-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="933ff-123">1,0</span><span class="sxs-lookup"><span data-stu-id="933ff-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="933ff-124">n/v</span><span class="sxs-lookup"><span data-stu-id="933ff-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="933ff-125">–</span><span class="sxs-lookup"><span data-stu-id="933ff-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="933ff-126">n/v</span><span class="sxs-lookup"><span data-stu-id="933ff-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="933ff-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933ff-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933ff-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="933ff-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="933ff-129">1.1</span><span class="sxs-lookup"><span data-stu-id="933ff-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="933ff-130">3.0</span><span class="sxs-lookup"><span data-stu-id="933ff-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="933ff-131">n/v</span><span class="sxs-lookup"><span data-stu-id="933ff-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="933ff-132">n/v</span><span class="sxs-lookup"><span data-stu-id="933ff-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="933ff-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933ff-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933ff-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="933ff-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="933ff-135">2.0</span><span class="sxs-lookup"><span data-stu-id="933ff-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="933ff-136">n/v</span><span class="sxs-lookup"><span data-stu-id="933ff-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="933ff-137">–</span><span class="sxs-lookup"><span data-stu-id="933ff-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="933ff-138">n/v</span><span class="sxs-lookup"><span data-stu-id="933ff-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="933ff-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933ff-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933ff-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="933ff-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="933ff-141">n/v</span><span class="sxs-lookup"><span data-stu-id="933ff-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="933ff-142">4.0 (16-Bit)</span><span class="sxs-lookup"><span data-stu-id="933ff-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="933ff-143">n/v</span><span class="sxs-lookup"><span data-stu-id="933ff-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="933ff-144">n/v</span><span class="sxs-lookup"><span data-stu-id="933ff-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="933ff-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933ff-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933ff-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="933ff-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="933ff-147">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="933ff-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="933ff-148">4.0 (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="933ff-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="933ff-149">' 95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="933ff-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="933ff-150">4.x</span><span class="sxs-lookup"><span data-stu-id="933ff-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="933ff-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933ff-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933ff-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="933ff-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="933ff-153">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="933ff-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="933ff-154">5.0</span><span class="sxs-lookup"><span data-stu-id="933ff-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="933ff-155">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="933ff-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="933ff-156">5.0</span><span class="sxs-lookup"><span data-stu-id="933ff-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="933ff-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933ff-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933ff-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="933ff-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="933ff-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="933ff-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="933ff-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="933ff-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="933ff-161">Microsoft Access-Datenbank-Engine</span><span class="sxs-lookup"><span data-stu-id="933ff-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="933ff-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="933ff-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="933ff-163">2007</span><span class="sxs-lookup"><span data-stu-id="933ff-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

