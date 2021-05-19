---
title: Zelle "Calendar" (Abschnitt "Text Fields")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60029
localization_priority: Normal
ms.assetid: 0c3e275e-25f0-3681-03f4-257145c19690
description: Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date ist.
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424753"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="800bf-103">Zelle "Calendar" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="800bf-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="800bf-104">Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date ist.</span><span class="sxs-lookup"><span data-stu-id="800bf-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="800bf-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="800bf-105">Remarks</span></span>

<span data-ttu-id="800bf-106">Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert).</span><span class="sxs-lookup"><span data-stu-id="800bf-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="800bf-107">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Calendar anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="800bf-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="800bf-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="800bf-108">Cell name:</span></span>  <br/> | <span data-ttu-id="800bf-109">Fields.Calendar[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="800bf-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="800bf-110">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Calendar nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="800bf-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="800bf-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="800bf-111">Section index:</span></span>  <br/> |<span data-ttu-id="800bf-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="800bf-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="800bf-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="800bf-113">Row index:</span></span>  <br/> |<span data-ttu-id="800bf-114">**visRowField**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="800bf-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="800bf-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="800bf-115">Cell index:</span></span>  <br/> |<span data-ttu-id="800bf-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="800bf-116">**visFieldCalendar**</span></span> <br/> |
   

