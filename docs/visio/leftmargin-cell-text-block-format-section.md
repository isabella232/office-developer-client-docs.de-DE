---
title: Zelle "LeftMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Bestimmt den Abstand zwischen dem linken Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der linke Rand unverändert.
ms.openlocfilehash: fee8eca8b5730e40518babe0c76549e10bebd902
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411337"
---
# <a name="leftmargin-cell-text-block-format-section"></a><span data-ttu-id="1832d-106">Zelle "LeftMargin" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="1832d-106">LeftMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="1832d-p102">Bestimmt den Abstand zwischen dem linken Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der linke Rand unverändert.</span><span class="sxs-lookup"><span data-stu-id="1832d-p102">Determines the distance between the left border of the text block and the text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the left margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1832d-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1832d-111">Remarks</span></span>

<span data-ttu-id="1832d-112">Um einen Verweis auf die Zelle LeftMargin anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="1832d-112">To get a reference to the LeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1832d-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1832d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="1832d-114">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="1832d-114">LeftMargin</span></span>  <br/> |
   
<span data-ttu-id="1832d-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LeftMargin nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="1832d-115">To get a reference to the LeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1832d-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1832d-116">Section index:</span></span>  <br/> |<span data-ttu-id="1832d-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1832d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1832d-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1832d-118">Row index:</span></span>  <br/> |<span data-ttu-id="1832d-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="1832d-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="1832d-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1832d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="1832d-121">**visTxtBlkLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="1832d-121">**visTxtBlkLeftMargin**</span></span> <br/> |
   

