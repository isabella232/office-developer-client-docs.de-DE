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
ms.openlocfilehash: 2bca91fd2efc283bcc8f2c5037c4d81dd9bcffc5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796558"
---
# <a name="calendar-cell-miscellaneous-section"></a><span data-ttu-id="ecd6a-103">Calendar Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="ecd6a-103">Calendar Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ecd6a-104">Bestimmt den Kalender, der verwendet wird, wenn eine Zellformel Datumsinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="ecd6a-104">Determines the calendar that is used when a cell formula contains Date information.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ecd6a-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ecd6a-105">Remarks</span></span>

<span data-ttu-id="ecd6a-106">Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert).</span><span class="sxs-lookup"><span data-stu-id="ecd6a-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="ecd6a-107">Wenn Sie einen Verweis auf die Zelle Calendar nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ecd6a-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ecd6a-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ecd6a-108">Cell name:</span></span>  <br/> | <span data-ttu-id="ecd6a-109">Calendar</span><span class="sxs-lookup"><span data-stu-id="ecd6a-109">Calendar</span></span>  <br/> |
   
<span data-ttu-id="ecd6a-110">Wenn Sie einen Verweis auf die Zelle Calendar aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ecd6a-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ecd6a-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ecd6a-111">Section index:</span></span>  <br/> |<span data-ttu-id="ecd6a-112">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ecd6a-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ecd6a-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ecd6a-113">Row index:</span></span>  <br/> |<span data-ttu-id="ecd6a-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="ecd6a-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="ecd6a-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ecd6a-115">Cell index:</span></span>  <br/> |<span data-ttu-id="ecd6a-116">**visObjCalendar**</span><span class="sxs-lookup"><span data-stu-id="ecd6a-116">**visObjCalendar**</span></span> <br/> |
   

