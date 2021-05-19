---
title: Zelle "SpBefore" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, vor jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den ersten Absatz in einem Textblock handelt (die Zelle TopMargin).
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425757"
---
# <a name="spbefore-cell-paragraph-section"></a><span data-ttu-id="2e506-103">Zelle "SpBefore" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="2e506-103">SpBefore Cell (Paragraph Section)</span></span>

<span data-ttu-id="2e506-104">Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, vor jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den ersten Absatz in einem Textblock handelt (die Zelle TopMargin).</span><span class="sxs-lookup"><span data-stu-id="2e506-104">Determines the amount of space inserted before each paragraph in the shape's text block, in addition to any space from the SpLine cell if it is the first paragraph in a text block, the TopMargin cell.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e506-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e506-105">Remarks</span></span>

<span data-ttu-id="2e506-p101">Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn es sich um eine skalierte Zeichnung handelt, bleibt die Einstellung für Abstand vor unverändert.</span><span class="sxs-lookup"><span data-stu-id="2e506-p101">This value is independent of the scale of the drawing. If the drawing is scaled, the Space Before setting remains the same.</span></span>
  
<span data-ttu-id="2e506-108">Um einen Verweis auf die Zelle SpBefore anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2e506-108">To get a reference to the SpBefore cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e506-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2e506-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2e506-110">Para.SpBefore[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2e506-110">Para.SpBefore[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2e506-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle SpBefore nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2e506-111">To get a reference to the SpBefore cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e506-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2e506-112">Section index:</span></span>  <br/> |<span data-ttu-id="2e506-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="2e506-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="2e506-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2e506-114">Row index:</span></span>  <br/> |<span data-ttu-id="2e506-115">**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2e506-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2e506-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2e506-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2e506-117">**visSpaceBefore**</span><span class="sxs-lookup"><span data-stu-id="2e506-117">**visSpaceBefore**</span></span> <br/> |
   

