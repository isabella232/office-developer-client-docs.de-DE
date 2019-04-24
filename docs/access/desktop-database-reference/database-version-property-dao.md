---
title: Database. Version-Eigenschaft (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41b408f63522902fd1d4f806090eef7563a3492a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294652"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="250ee-102">Database. Version-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="250ee-102">Database.Version property (DAO)</span></span>

<span data-ttu-id="250ee-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="250ee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="250ee-104">In einem Microsoft Access-Arbeitsbereich gibt diese Eigenschaft die Version der Microsoft Jet- oder Microsoft Access-Datenbank-Engine zurück, mit der die Datenbank erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="250ee-104">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database.</span></span> <span data-ttu-id="250ee-105">Schreibgeschützter **String**-Wert.</span><span class="sxs-lookup"><span data-stu-id="250ee-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="250ee-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="250ee-106">Syntax</span></span>

<span data-ttu-id="250ee-107">*Ausdruck* . Version</span><span class="sxs-lookup"><span data-stu-id="250ee-107">*expression* .Version</span></span>

<span data-ttu-id="250ee-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="250ee-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="250ee-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="250ee-109">Remarks</span></span>

<span data-ttu-id="250ee-110">Der Rückgabewert ist ein String-Datentyp, der als Versionsnummer im folgenden Format ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="250ee-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

- <span data-ttu-id="250ee-111">Microsoft Access-Arbeitsbereich stellt die Versionsnummer im Format "*Major. Minor*" dar.</span><span class="sxs-lookup"><span data-stu-id="250ee-111">Microsoft Access workspace represents the version number in the form "*major.minor*".</span></span> <span data-ttu-id="250ee-112">For example, "3.0".</span><span class="sxs-lookup"><span data-stu-id="250ee-112">For example, "3.0".</span></span> <span data-ttu-id="250ee-113">The product version number consists of the version number (3), a period, and the release number (0).</span><span class="sxs-lookup"><span data-stu-id="250ee-113">The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="250ee-114">Die folgende Tabelle zeigt, welche Version der Datenbank-Engine in verschiedenen Versionen von Microsoft-Produkten enthalten waren.</span><span class="sxs-lookup"><span data-stu-id="250ee-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

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
<th><p><span data-ttu-id="250ee-115">Datenbank-Engine</span><span class="sxs-lookup"><span data-stu-id="250ee-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="250ee-116">Version (Freigabejahr)</span><span class="sxs-lookup"><span data-stu-id="250ee-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="250ee-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="250ee-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="250ee-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="250ee-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="250ee-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="250ee-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="250ee-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="250ee-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="250ee-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="250ee-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="250ee-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="250ee-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="250ee-123">1.0</span><span class="sxs-lookup"><span data-stu-id="250ee-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="250ee-124">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="250ee-125">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="250ee-126">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="250ee-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="250ee-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="250ee-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="250ee-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="250ee-129">1.1</span><span class="sxs-lookup"><span data-stu-id="250ee-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="250ee-130">3,0</span><span class="sxs-lookup"><span data-stu-id="250ee-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="250ee-131">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="250ee-132">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="250ee-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="250ee-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="250ee-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="250ee-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="250ee-135">2.0</span><span class="sxs-lookup"><span data-stu-id="250ee-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="250ee-136">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="250ee-137">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="250ee-138">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="250ee-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="250ee-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="250ee-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="250ee-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="250ee-141">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="250ee-142">4.0 (16-Bit)</span><span class="sxs-lookup"><span data-stu-id="250ee-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="250ee-143">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="250ee-144">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="250ee-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="250ee-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="250ee-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="250ee-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="250ee-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="250ee-147">‘ 95 (7.0)’</span><span class="sxs-lookup"><span data-stu-id="250ee-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="250ee-148">4.0 (32-Bit)</span><span class="sxs-lookup"><span data-stu-id="250ee-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="250ee-149">‘ 95 (7.0)’</span><span class="sxs-lookup"><span data-stu-id="250ee-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="250ee-150">4. x</span><span class="sxs-lookup"><span data-stu-id="250ee-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="250ee-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="250ee-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="250ee-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="250ee-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="250ee-153">‘ 97 (8.0)’</span><span class="sxs-lookup"><span data-stu-id="250ee-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="250ee-154">5,0</span><span class="sxs-lookup"><span data-stu-id="250ee-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="250ee-155">‘ 97 (8.0)’</span><span class="sxs-lookup"><span data-stu-id="250ee-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="250ee-156">5,0</span><span class="sxs-lookup"><span data-stu-id="250ee-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="250ee-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="250ee-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="250ee-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="250ee-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="250ee-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="250ee-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="250ee-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="250ee-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="250ee-161">Microsoft Access-Datenbank-Engine</span><span class="sxs-lookup"><span data-stu-id="250ee-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="250ee-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="250ee-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="250ee-163">2007</span><span class="sxs-lookup"><span data-stu-id="250ee-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

