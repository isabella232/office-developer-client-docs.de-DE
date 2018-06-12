---
title: Zelle "IndLeft" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom linken Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der linke Einzug gleich.
ms.openlocfilehash: 2ccccfdeacc73539c612790613c7eca85de55b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797201"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="b5cec-105">Zelle "IndLeft" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="b5cec-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="b5cec-p102">Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom linken Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der linke Einzug gleich.</span><span class="sxs-lookup"><span data-stu-id="b5cec-p102">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b5cec-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5cec-109">Remarks</span></span>

<span data-ttu-id="b5cec-110">Wenn Sie einen Verweis auf die Zelle IndLeft nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b5cec-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5cec-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b5cec-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b5cec-112">Para.IndLeft [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b5cec-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b5cec-113">Wenn Sie einen Verweis auf die Zelle IndLeft aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b5cec-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b5cec-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b5cec-114">Section index:</span></span>  <br/> |<span data-ttu-id="b5cec-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="b5cec-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="b5cec-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b5cec-116">Row index:</span></span>  <br/> |<span data-ttu-id="b5cec-117">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b5cec-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b5cec-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b5cec-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b5cec-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="b5cec-119">**visIndentLeft**</span></span> <br/> |
   

