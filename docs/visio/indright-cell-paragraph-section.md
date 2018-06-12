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
ms.openlocfilehash: 83f2688e598ffb335a9fafd1eed56ea17ffd4b2f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797203"
---
# <a name="indright-cell-paragraph-section"></a><span data-ttu-id="faae8-105">Zelle "IndRight" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="faae8-105">IndRight Cell (Paragraph Section)</span></span>

<span data-ttu-id="faae8-p102">Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom rechten Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der rechte Einzug gleich.</span><span class="sxs-lookup"><span data-stu-id="faae8-p102">Represents the distance all lines of text in a paragraph are indented from the right margin of the text block. This value is independent of the scale of the drawing. If the drawing is scaled, the right indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="faae8-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="faae8-109">Remarks</span></span>

<span data-ttu-id="faae8-110">Wenn Sie einen Verweis auf die Zelle IndRight nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="faae8-110">To get a reference to the IndRight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="faae8-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="faae8-111">Cell name:</span></span>  <br/> | <span data-ttu-id="faae8-112">Para.IndRight [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="faae8-112">Para.IndRight[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="faae8-113">Wenn Sie einen Verweis auf die Zelle IndRight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="faae8-113">To get a reference to the IndRight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="faae8-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="faae8-114">Section index:</span></span>  <br/> |<span data-ttu-id="faae8-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="faae8-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="faae8-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="faae8-116">Row index:</span></span>  <br/> |<span data-ttu-id="faae8-117">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="faae8-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="faae8-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="faae8-118">Cell index:</span></span>  <br/> |<span data-ttu-id="faae8-119">**visIndentRight**</span><span class="sxs-lookup"><span data-stu-id="faae8-119">**visIndentRight**</span></span> <br/> |
   

