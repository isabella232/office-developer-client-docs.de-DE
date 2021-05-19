---
title: Zelle "TheText" (Abschnitt "Events")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: Eine Ereigniszelle, die berechnet wird, wenn der Text oder die Textgestaltung eines Shapes geändert wird.
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435166"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="c089b-103">Zelle "TheText" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="c089b-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="c089b-104">Eine Ereigniszelle, die berechnet wird, wenn der Text oder die Textgestaltung eines Shapes geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c089b-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c089b-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c089b-105">Remarks</span></span>

<span data-ttu-id="c089b-p101">Ereigniszellen werden nur beim Eintreffen des Ereignisses, nicht bei der Formeleingabe ausgewertet. Sie können die Zelle TheText verwenden, um Neuberechnungen zu starten, beispielsweise um die Textbreite und -höhe mithilfe der Funktionen TEXTWIDTH( ) und TEXTHÖHE( ) neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="c089b-p101">Event cells are evaluated only when the event occurs, not upon formula entry. You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="c089b-108">Um einen Verweis auf die Zelle TheText anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="c089b-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c089b-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c089b-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c089b-110">TheText</span><span class="sxs-lookup"><span data-stu-id="c089b-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="c089b-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TheText nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c089b-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c089b-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c089b-112">Section index:</span></span>  <br/> |<span data-ttu-id="c089b-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c089b-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c089b-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c089b-114">Row index:</span></span>  <br/> |<span data-ttu-id="c089b-115">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="c089b-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="c089b-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c089b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c089b-117">**visEvtCellTheText**</span><span class="sxs-lookup"><span data-stu-id="c089b-117">**visEvtCellTheText**</span></span> <br/> |
   

