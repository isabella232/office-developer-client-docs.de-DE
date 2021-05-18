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
# <a name="calendar-cell-miscellaneous-section"></a><span data-ttu-id="985a9-103">Zelle "Calendar" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="985a9-103">Calendar Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="985a9-104">Bestimmt den Kalender, der verwendet wird, wenn eine Zellformel Datumsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="985a9-104">Determines the calendar that is used when a cell formula contains Date information.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="985a9-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="985a9-105">Remarks</span></span>

<span data-ttu-id="985a9-106">Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert).</span><span class="sxs-lookup"><span data-stu-id="985a9-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="985a9-107">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Calendar anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="985a9-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="985a9-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="985a9-108">Cell name:</span></span>  <br/> | <span data-ttu-id="985a9-109">Kalender</span><span class="sxs-lookup"><span data-stu-id="985a9-109">Calendar</span></span>  <br/> |
   
<span data-ttu-id="985a9-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Calendar nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="985a9-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="985a9-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="985a9-111">Section index:</span></span>  <br/> |<span data-ttu-id="985a9-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="985a9-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="985a9-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="985a9-113">Row index:</span></span>  <br/> |<span data-ttu-id="985a9-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="985a9-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="985a9-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="985a9-115">Cell index:</span></span>  <br/> |<span data-ttu-id="985a9-116">**visObjCalendar**</span><span class="sxs-lookup"><span data-stu-id="985a9-116">**visObjCalendar**</span></span> <br/> |
   

