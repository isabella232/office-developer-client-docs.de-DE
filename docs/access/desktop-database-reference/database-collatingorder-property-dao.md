---
title: Database.CollatingOrder Property (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6101729af7f77e1451de240deece2bf789110fb7
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2018
ms.locfileid: "25475173"
---
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="e763e-102">Database.CollatingOrder Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="e763e-102">Database.CollatingOrder Property (DAO)</span></span>


<span data-ttu-id="e763e-103">**Betrifft**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="e763e-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e763e-p101">Gibt einen Wert zurück, der die Sequenz der Sortierreihenfolge im Text für den Zeichenfolgenvergleich oder die Sortierung angibt (gilt nur für Microsoft Access-Arbeitsbereiche). Schreibgeschützter **Long**-Wert.</span><span class="sxs-lookup"><span data-stu-id="e763e-p101">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only). Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="e763e-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e763e-106">Syntax</span></span>

<span data-ttu-id="e763e-107">*Ausdruck* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="e763e-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="e763e-108">*Ausdruck* Eine Variable, die ein **Database** -Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="e763e-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e763e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e763e-109">Remarks</span></span>

<span data-ttu-id="e763e-110">Der Rückgabewert ist ein **Long**-Wert oder eine Konstante, die einem der folgenden Werte entsprechen kann.</span><span class="sxs-lookup"><span data-stu-id="e763e-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e763e-111">Konstante</span><span class="sxs-lookup"><span data-stu-id="e763e-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="e763e-112">Sortierreihenfolge</span><span class="sxs-lookup"><span data-stu-id="e763e-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e763e-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-114">Allgemein (Englisch, Französisch, Deutsch, Portugiesisch, Italienisch und modernes Spanisch)</span><span class="sxs-lookup"><span data-stu-id="e763e-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-116">Arabisch</span><span class="sxs-lookup"><span data-stu-id="e763e-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-118">Chinesisch (Vereinfacht)</span><span class="sxs-lookup"><span data-stu-id="e763e-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-120">Chinesisch (Traditionell)</span><span class="sxs-lookup"><span data-stu-id="e763e-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-122">Russisch</span><span class="sxs-lookup"><span data-stu-id="e763e-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-124">Tschechisch</span><span class="sxs-lookup"><span data-stu-id="e763e-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-126">Niederländisch</span><span class="sxs-lookup"><span data-stu-id="e763e-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-128">Griechisch</span><span class="sxs-lookup"><span data-stu-id="e763e-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-130">Hebräisch</span><span class="sxs-lookup"><span data-stu-id="e763e-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-132">Ungarisch</span><span class="sxs-lookup"><span data-stu-id="e763e-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-134">Isländisch</span><span class="sxs-lookup"><span data-stu-id="e763e-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-136">Japanisch</span><span class="sxs-lookup"><span data-stu-id="e763e-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-138">Koreanisch</span><span class="sxs-lookup"><span data-stu-id="e763e-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-140">Neutral</span><span class="sxs-lookup"><span data-stu-id="e763e-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-142">Norwegisch oder Dänisch</span><span class="sxs-lookup"><span data-stu-id="e763e-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="e763e-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-146">Paradox Norwegisch oder Dänisch</span><span class="sxs-lookup"><span data-stu-id="e763e-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-148">Paradox Schwedisch oder Finnisch</span><span class="sxs-lookup"><span data-stu-id="e763e-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-150">Polnisch</span><span class="sxs-lookup"><span data-stu-id="e763e-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-152">Slowenisch</span><span class="sxs-lookup"><span data-stu-id="e763e-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-154">Spanisch</span><span class="sxs-lookup"><span data-stu-id="e763e-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-156">Schwedisch oder Finnisch</span><span class="sxs-lookup"><span data-stu-id="e763e-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-158">Thailändisch</span><span class="sxs-lookup"><span data-stu-id="e763e-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e763e-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-160">Türkisch</span><span class="sxs-lookup"><span data-stu-id="e763e-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e763e-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="e763e-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="e763e-162">Nicht definiert oder unbekannt</span><span class="sxs-lookup"><span data-stu-id="e763e-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e763e-163">Die Einstellung der **CollatingOrder** -Eigenschaft entspricht dem Argument Locale der **CreateDatabase** -Methode, wenn die Datenbank erstellt wurde oder der **CompactDatabase** -Methode, wenn die Datenbank kürzlich komprimiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e763e-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="e763e-p102">Überprüfen Sie die Einstellung der **CollatingOrder**-Eigenschaft eines **Database**- oder **Field**-Objekts, um die Methode des Zeichenfolgenvergleichs für die Datenbank oder das Feld zu ermitteln. Sie können die **CollatingOrder**-Eigenschaft eines neuen, noch nicht angefügten **Field**-Objekts festlegen, wenn sich die Einstellung des **Field**-Objekts und des **Database**-Objekts, in dem es enthalten ist, unterscheiden soll.</span><span class="sxs-lookup"><span data-stu-id="e763e-p102">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field. You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

