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
ms.openlocfilehash: 6d9d3ef0addb1d6081e2046ca7a5a663eb2a9c8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796548"
---
# <a name="calendar-cell-text-fields-section"></a><span data-ttu-id="b63a2-103">Calendar Cell (Text Fields Section)</span><span class="sxs-lookup"><span data-stu-id="b63a2-103">Calendar Cell (Text Fields Section)</span></span>

<span data-ttu-id="b63a2-104">Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date lautet.</span><span class="sxs-lookup"><span data-stu-id="b63a2-104">Determines the calendar that is used for a text field when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b63a2-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b63a2-105">Remarks</span></span>

<span data-ttu-id="b63a2-106">Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert).</span><span class="sxs-lookup"><span data-stu-id="b63a2-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="b63a2-107">Wenn Sie einen Verweis auf die Zelle Calendar nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b63a2-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b63a2-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b63a2-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b63a2-109">Fields.Calendar [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b63a2-109">Fields.Calendar[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b63a2-110">Wenn Sie einen Verweis auf die Zelle Calendar aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b63a2-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b63a2-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b63a2-111">Section index:</span></span>  <br/> |<span data-ttu-id="b63a2-112">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="b63a2-112">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="b63a2-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b63a2-113">Row index:</span></span>  <br/> |<span data-ttu-id="b63a2-114">**VisRowField** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b63a2-114">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b63a2-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b63a2-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b63a2-116">**visFieldCalendar**</span><span class="sxs-lookup"><span data-stu-id="b63a2-116">**visFieldCalendar**</span></span> <br/> |
   

