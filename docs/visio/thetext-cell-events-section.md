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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326677"
---
# <a name="thetext-cell-events-section"></a><span data-ttu-id="ddf73-103">Zelle "TheText" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="ddf73-103">TheText Cell (Events Section)</span></span>

<span data-ttu-id="ddf73-104">Eine Ereigniszelle, die berechnet wird, wenn der Text oder die Textgestaltung eines Shapes geändert wird.</span><span class="sxs-lookup"><span data-stu-id="ddf73-104">An event cell that is evaluated when a shape's text or text composition changes.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ddf73-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddf73-105">Remarks</span></span>

<span data-ttu-id="ddf73-p101">Ereigniszellen werden nur beim Eintreffen des Ereignisses, nicht bei der Formeleingabe ausgewertet. Sie können die Zelle TheText verwenden, um Neuberechnungen zu starten, beispielsweise um die Textbreite und -höhe mithilfe der Funktionen TEXTWIDTH( ) und TEXTHÖHE( ) neu zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="ddf73-p101">Event cells are evaluated only when the event occurs, not upon formula entry. You can use the TheText cell to trigger recalculations, for example, to recalculate the text width and height with the TEXTWIDTH( ) and TEXTHEIGHT( ) functions.</span></span>
  
<span data-ttu-id="ddf73-108">Wenn Sie einen Verweis auf die Zelle DerText aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ddf73-108">To get a reference to the TheText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddf73-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ddf73-109">Cell name:</span></span>  <br/> | <span data-ttu-id="ddf73-110">DerText</span><span class="sxs-lookup"><span data-stu-id="ddf73-110">TheText</span></span>  <br/> |
   
<span data-ttu-id="ddf73-111">Wenn Sie einen Verweis auf die Zelle DerText aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ddf73-111">To get a reference to the TheText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddf73-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ddf73-112">Section index:</span></span>  <br/> |<span data-ttu-id="ddf73-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ddf73-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ddf73-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ddf73-114">Row index:</span></span>  <br/> |<span data-ttu-id="ddf73-115">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="ddf73-115">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="ddf73-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ddf73-116">Cell index:</span></span>  <br/> |<span data-ttu-id="ddf73-117">**visEvtCellTheText**</span><span class="sxs-lookup"><span data-stu-id="ddf73-117">**visEvtCellTheText**</span></span> <br/> |
   

