---
title: Database. CollatingOrder-Eigenschaft (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21d775c0abac5d2afddd6b0930816c8d6d381ff0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295016"
---
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="4fb00-102">Database. CollatingOrder-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="4fb00-102">Database.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="4fb00-103">**Gilt für**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4fb00-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4fb00-p101">Gibt einen Wert zurück, der die Sequenz der Sortierreihenfolge im Text für den Zeichenfolgenvergleich oder die Sortierung angibt (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Long**-Wert.</span><span class="sxs-lookup"><span data-stu-id="4fb00-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fb00-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fb00-106">Syntax</span></span>

<span data-ttu-id="4fb00-107">*Ausdruck* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="4fb00-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="4fb00-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="4fb00-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4fb00-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4fb00-109">Remarks</span></span>

<span data-ttu-id="4fb00-110">Der Rückgabewert ist ein **Long**-Wert oder eine Konstante, die einem der folgenden Werte entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="4fb00-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4fb00-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="4fb00-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="4fb00-112">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="4fb00-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-114">Allgemein (Englisch, Französisch, Deutsch, Portugiesisch, Italienisch und modernes Spanisch)</span><span class="sxs-lookup"><span data-stu-id="4fb00-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-116">Arabisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-118">Chinesisch (Vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="4fb00-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-120">Traditionelles Chinesisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-122">Russisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-124">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-126">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-128">Griechisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-130">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-132">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-134">Isländisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-136">Japanisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-138">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-140">Neutral</span><span class="sxs-lookup"><span data-stu-id="4fb00-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-142">Norwegisch oder Dänisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="4fb00-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-146">Paradox Norwegisch oder Dänisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-148">Paradox Schwedisch oder Finnisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-150">Polnisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-152">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-154">Spanisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-156">Schwedisch oder Finnisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-158">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4fb00-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-160">Türkisch</span><span class="sxs-lookup"><span data-stu-id="4fb00-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4fb00-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="4fb00-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="4fb00-162">Nicht definiert oder unbekannt</span><span class="sxs-lookup"><span data-stu-id="4fb00-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4fb00-163">Die Einstellung der **CollatingOrder** -Eigenschaft entspricht dem Argument locale \*\*\*\* der CreateDatabase-Methode, wenn die Datenbank erstellt wurde, oder die **CompactDatabase** -Methode, wenn die Datenbank zuletzt komprimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="4fb00-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="4fb00-p102">Überprüfen Sie die Einstellung der **CollatingOrder**-Eigenschaft eines **Database**- oder **Field**-Objekts, um die Methode des Zeichenfolgenvergleichs für die Datenbank oder das Feld zu ermitteln. Sie können die **CollatingOrder**-Eigenschaft eines neuen, noch nicht angefügten **Field**-Objekts festlegen, wenn sich die Einstellung des **Field**-Objekts und des **Database**-Objekts, in dem es enthalten ist, unterscheiden soll.</span><span class="sxs-lookup"><span data-stu-id="4fb00-p102">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field. You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

