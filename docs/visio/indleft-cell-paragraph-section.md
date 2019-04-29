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
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405163"
---
# <a name="indleft-cell-paragraph-section"></a><span data-ttu-id="ae868-105">Zelle "IndLeft" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="ae868-105">IndLeft Cell (Paragraph Section)</span></span>

<span data-ttu-id="ae868-p102">Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom linken Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der linke Einzug gleich.</span><span class="sxs-lookup"><span data-stu-id="ae868-p102">Represents the distance all lines of text in a paragraph are indented from the left margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the left indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae868-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ae868-109">Remarks</span></span>

<span data-ttu-id="ae868-110">Wenn Sie einen Verweis auf die Zelle IndLeft aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ae868-110">To get a reference to the IndLeft cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae868-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ae868-111">Cell name:</span></span>  <br/> | <span data-ttu-id="ae868-112">Abs. IndLeft [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ae868-112">Para.IndLeft[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ae868-113">Wenn Sie einen Verweis auf die Zelle IndLeft aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ae868-113">To get a reference to the IndLeft cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ae868-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ae868-114">Section index:</span></span>  <br/> |<span data-ttu-id="ae868-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="ae868-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="ae868-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ae868-116">Row index:</span></span>  <br/> |<span data-ttu-id="ae868-117">**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ae868-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ae868-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ae868-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ae868-119">**visIndentLeft**</span><span class="sxs-lookup"><span data-stu-id="ae868-119">**visIndentLeft**</span></span> <br/> |
   

