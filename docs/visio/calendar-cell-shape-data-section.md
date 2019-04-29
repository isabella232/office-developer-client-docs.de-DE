---
title: Zelle "Calendar" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60027
localization_priority: Normal
ms.assetid: f5dcc6d9-474a-9ecb-21f5-56415d934890
description: Bestimmt den Kalender, der für Shape-Daten verwendet wird, wenn der Datentyp Date lautet.
ms.openlocfilehash: 2ddbd578053e2ae37514194450bd95dc9cdf441d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432758"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="88477-103">Zelle "Calendar" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="88477-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="88477-104">Bestimmt den Kalender, der für Shape-Daten verwendet wird, wenn der Datentyp Date lautet.</span><span class="sxs-lookup"><span data-stu-id="88477-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88477-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="88477-105">Remarks</span></span>

<span data-ttu-id="88477-106">Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert).</span><span class="sxs-lookup"><span data-stu-id="88477-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="88477-107">Wenn Sie einen Verweis auf die Zelle Calendar aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="88477-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="88477-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="88477-108">Cell name:</span></span>  <br/> | <span data-ttu-id="88477-109">Prop.  *Name* . Kalender, wobei Prop.  *Name* ist der Name der Zeile</span><span class="sxs-lookup"><span data-stu-id="88477-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="88477-110">Wenn Sie einen Verweis auf die Zelle Calendar aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="88477-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="88477-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="88477-111">Section index:</span></span>  <br/> |<span data-ttu-id="88477-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="88477-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="88477-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="88477-113">Row index:</span></span>  <br/> |<span data-ttu-id="88477-114">**visRowProp** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="88477-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="88477-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="88477-115">Cell index:</span></span>  <br/> |<span data-ttu-id="88477-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="88477-116">**visCustPropsCalendar**</span></span> <br/> |
   

