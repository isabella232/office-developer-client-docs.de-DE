---
title: Field.CollatingOrder-Eigenschaft (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: a2607ace-a660-899b-eae8-4612ce2f87f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820980(v=office.15)
ms:contentKeyID: 48546758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052897
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d64620ccf1c0d011c060ac829223041f49bde9d1
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/02/2018
ms.locfileid: "25925289"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="a35c7-102">Field.CollatingOrder-Eigenschaft (DAO)</span><span class="sxs-lookup"><span data-stu-id="a35c7-102">Field.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="a35c7-103">**Betrifft**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a35c7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a35c7-p101">Gibt einen Wert zurück, der die Sequenz der Sortierreihenfolge im Text für den Zeichenfolgenvergleich oder die Sortierung angibt (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Long**-Wert.</span><span class="sxs-lookup"><span data-stu-id="a35c7-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a35c7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a35c7-106">Syntax</span></span>

<span data-ttu-id="a35c7-107">*Ausdruck* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="a35c7-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="a35c7-108">*Ausdruck* Eine Variable, die ein **Field** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="a35c7-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a35c7-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a35c7-109">Remarks</span></span>

<span data-ttu-id="a35c7-110">Der Rückgabewert ist ein **Long**-Wert oder eine Konstante, die einem der folgenden Werte entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="a35c7-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a35c7-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="a35c7-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="a35c7-112">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="a35c7-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-114">Allgemein (Englisch, Französisch, Deutsch, Portugiesisch, Italienisch und modernes Spanisch)</span><span class="sxs-lookup"><span data-stu-id="a35c7-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-116">Arabisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-118">Chinesisch (Vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="a35c7-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-120">Chinesisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="a35c7-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-122">Russisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-124">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-126">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-128">Griechisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-130">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-132">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-134">Isländisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-136">Japanisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-138">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-140">Neutral</span><span class="sxs-lookup"><span data-stu-id="a35c7-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-142">Norwegisch oder Dänisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="a35c7-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-146">Paradox Norwegisch oder Dänisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-148">Paradox Schwedisch oder Finnisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-150">Polnisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-152">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-154">Spanisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-156">Schwedisch oder Finnisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-158">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-160">Türkisch</span><span class="sxs-lookup"><span data-stu-id="a35c7-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="a35c7-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="a35c7-162">Nicht definiert oder unbekannt</span><span class="sxs-lookup"><span data-stu-id="a35c7-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a35c7-163">Die Verfügbarkeit der **CollatingOrder**-Eigenschaft hängt vom Objekt ab, in dem die **Fields**-Auflistung enthalten ist (siehe folgende Tabelle).</span><span class="sxs-lookup"><span data-stu-id="a35c7-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a35c7-164">Zugehörigkeit der Fields-Auflistung</span><span class="sxs-lookup"><span data-stu-id="a35c7-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="a35c7-165">Verfügbarkeit von CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="a35c7-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-166"><strong>Index</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="a35c7-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a35c7-167">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a35c7-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-168"><strong>QueryDef</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="a35c7-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a35c7-169">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a35c7-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-170"><strong>Recordset</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="a35c7-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a35c7-171">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a35c7-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a35c7-172"><strong>Relation</strong> -Objekt</span><span class="sxs-lookup"><span data-stu-id="a35c7-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a35c7-173">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a35c7-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a35c7-174"><strong>TableDef</strong>-Objekt</span><span class="sxs-lookup"><span data-stu-id="a35c7-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a35c7-175">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a35c7-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a35c7-176">Die Einstellung der **CollatingOrder** -Eigenschaft entspricht dem Argument Locale der **CreateDatabase** -Methode, wenn die Datenbank erstellt wurde oder der **CompactDatabase** -Methode, wenn die Datenbank kürzlich komprimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="a35c7-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="a35c7-p102">Die Einstellungen der Eigenschaften **CollatingOrder** und **Attributes** eines **Field**-Objekts in einer **Fields**-Auflistung eines **Index** bestimmen zusammen die Sequenz und Richtung der Sortierreihenfolge in einem Index. Die Sortierreihenfolge kann nicht für einen einzelnen Index festgelegt werden, sondern nur für eine gesamte Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a35c7-p102">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index. However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

