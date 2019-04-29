---
title: Zelle "Calendar" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60028
localization_priority: Normal
ms.assetid: 7406b46d-b42d-187c-70e8-123c4da7e781
description: Bestimmt den Kalender, der verwendet wird, wenn eine Zellformel Datumsinformationen enthält.
ms.openlocfilehash: f756b0d445bd3f90b67e0b1412bd7ac51a8cdb7e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421816"
---
# <a name="calendar-cell-miscellaneous-section"></a><span data-ttu-id="86de6-103">Zelle "Calendar" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="86de6-103">Calendar Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="86de6-104">Bestimmt den Kalender, der verwendet wird, wenn eine Zellformel Datumsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="86de6-104">Determines the calendar that is used when a cell formula contains Date information.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="86de6-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86de6-105">Remarks</span></span>

<span data-ttu-id="86de6-106">Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert).</span><span class="sxs-lookup"><span data-stu-id="86de6-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="86de6-107">Wenn Sie einen Verweis auf die Zelle Calendar aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="86de6-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86de6-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="86de6-108">Cell name:</span></span>  <br/> | <span data-ttu-id="86de6-109">Kalender</span><span class="sxs-lookup"><span data-stu-id="86de6-109">Calendar</span></span>  <br/> |
   
<span data-ttu-id="86de6-110">Wenn Sie einen Verweis auf die Zelle Calendar aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="86de6-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="86de6-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="86de6-111">Section index:</span></span>  <br/> |<span data-ttu-id="86de6-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="86de6-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="86de6-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="86de6-113">Row index:</span></span>  <br/> |<span data-ttu-id="86de6-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="86de6-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="86de6-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="86de6-115">Cell index:</span></span>  <br/> |<span data-ttu-id="86de6-116">**visObjCalendar**</span><span class="sxs-lookup"><span data-stu-id="86de6-116">**visObjCalendar**</span></span> <br/> |
   

