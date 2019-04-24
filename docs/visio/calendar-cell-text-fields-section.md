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
description: Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date lautet.
ms.openlocfilehash: e90f757fb176375c8f9e9d5744e09b67afaca527
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337499"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="0a77c-103">Zelle "Calendar" (Abschnitt "Text Fields")</span><span class="sxs-lookup"><span data-stu-id="0a77c-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="0a77c-104">Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date lautet.</span><span class="sxs-lookup"><span data-stu-id="0a77c-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0a77c-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0a77c-105">Remarks</span></span>

<span data-ttu-id="0a77c-106">Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert).</span><span class="sxs-lookup"><span data-stu-id="0a77c-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="0a77c-107">Wenn Sie einen Verweis auf die Zelle Calendar aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0a77c-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a77c-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0a77c-108">Cell name:</span></span>  <br/> | <span data-ttu-id="0a77c-109">Fields. Calendar [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0a77c-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0a77c-110">Wenn Sie einen Verweis auf die Zelle Calendar aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0a77c-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0a77c-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0a77c-111">Section index:</span></span>  <br/> |<span data-ttu-id="0a77c-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="0a77c-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="0a77c-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0a77c-113">Row index:</span></span>  <br/> |<span data-ttu-id="0a77c-114">**visRowField** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0a77c-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0a77c-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0a77c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0a77c-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="0a77c-116">**visFieldCalendar**</span></span> <br/> |
   

