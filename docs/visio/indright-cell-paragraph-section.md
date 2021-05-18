---
title: Zelle "IndRight" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom rechten Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der rechte Einzug gleich.
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408866"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="0d62d-105">Zelle "IndRight" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="0d62d-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="0d62d-p102">Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom rechten Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der rechte Einzug gleich.</span><span class="sxs-lookup"><span data-stu-id="0d62d-p102">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d62d-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d62d-109">Remarks</span></span>

<span data-ttu-id="0d62d-110">Um einen Verweis auf die Zelle IndRight anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="0d62d-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d62d-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0d62d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="0d62d-112">Para.IndRight[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0d62d-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0d62d-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die IndRight-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="0d62d-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d62d-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0d62d-114">Section index:</span></span>  <br/> |<span data-ttu-id="0d62d-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="0d62d-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="0d62d-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0d62d-116">Row index:</span></span>  <br/> |<span data-ttu-id="0d62d-117">**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0d62d-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0d62d-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0d62d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="0d62d-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="0d62d-119">**visIndentRight**</span></span> <br/> |
   

