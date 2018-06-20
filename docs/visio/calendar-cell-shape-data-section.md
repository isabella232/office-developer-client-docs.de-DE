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
ms.openlocfilehash: 502ecd8a028c4c0d9841bbd3e0ed369f73bd6b65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796568"
---
# <a name="calendar-cell-shape-data-section"></a><span data-ttu-id="6ed21-103">Zelle "Calendar" (Abschnitt "Shape Data")</span><span class="sxs-lookup"><span data-stu-id="6ed21-103">Calendar Cell (Shape Data Section)</span></span>

<span data-ttu-id="6ed21-104">Bestimmt den Kalender, der für Shape-Daten verwendet wird, wenn der Datentyp Date lautet.</span><span class="sxs-lookup"><span data-stu-id="6ed21-104">Determines the calendar that is used for shape data when the data type is Date.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6ed21-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ed21-105">Remarks</span></span>

<span data-ttu-id="6ed21-106">Die folgenden Werte sind möglich: 0 (Westlich), 1 (Arabisch Hijri), 2 (Hebräischer Mondkalender), 3 (Taiwankalender), 4 (Japan - Kaiserherrschaft), 5 (Thai Buddhistisch), 6 (Koreanisch Danki), 7 (Indischer Kalender), 8 (Englisch transkribiert) und 9 (Französisch transkribiert).</span><span class="sxs-lookup"><span data-stu-id="6ed21-106">The possible values are: 0 (Western), 1 (Arabic Hijri), 2 (Hebrew Lunar), 3 (Taiwan Calendar), 4 (Japanese Emperor Reign), 5 (Thai Buddhist), 6 (Korean Danki), 7 (Saka Era), 8 (English transliterated), and 9 (French transliterated ).</span></span> 
  
<span data-ttu-id="6ed21-107">Wenn Sie einen Verweis auf die Zelle Calendar nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6ed21-107">To get a reference to the Calendar cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ed21-108">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6ed21-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6ed21-109">Eigenschaft.  *Name* . Kalender wobei Prop.  *Name* ist der Zeilenname</span><span class="sxs-lookup"><span data-stu-id="6ed21-109">Prop.  *name*  .Calendar            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6ed21-110">Wenn Sie einen Verweis auf die Zelle Calendar aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6ed21-110">To get a reference to the Calendar cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ed21-111">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6ed21-111">Section index:</span></span>  <br/> |<span data-ttu-id="6ed21-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="6ed21-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="6ed21-113">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6ed21-113">Row index:</span></span>  <br/> |<span data-ttu-id="6ed21-114">**VisRowProp** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6ed21-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6ed21-115">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6ed21-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6ed21-116">**visCustPropsCalendar**</span><span class="sxs-lookup"><span data-stu-id="6ed21-116">**visCustPropsCalendar**</span></span> <br/> |
   

