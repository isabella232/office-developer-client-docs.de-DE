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
ms.openlocfilehash: d24ba33bffea1529490b49e105fec5d01cd828b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797308"
---
# <a name="leftmargin-cell-text-block-format-section"></a><span data-ttu-id="4eb32-106">LeftMargin Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="4eb32-106">LeftMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="4eb32-p102">Bestimmt den Abstand zwischen dem linken Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der linke Rand unverändert.</span><span class="sxs-lookup"><span data-stu-id="4eb32-p102">Determines the distance between the left border of the text block and the text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the left margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4eb32-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4eb32-111">Remarks</span></span>

<span data-ttu-id="4eb32-112">Wenn Sie einen Verweis auf die Zelle LeftMargin aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4eb32-112">To get a reference to the LeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4eb32-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4eb32-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4eb32-114">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="4eb32-114">LeftMargin</span></span>  <br/> |
   
<span data-ttu-id="4eb32-115">Wenn Sie einen Verweis auf die Zelle LeftMargin aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="4eb32-115">To get a reference to the LeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4eb32-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4eb32-116">Section index:</span></span>  <br/> |<span data-ttu-id="4eb32-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4eb32-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4eb32-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4eb32-118">Row index:</span></span>  <br/> |<span data-ttu-id="4eb32-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="4eb32-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="4eb32-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4eb32-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4eb32-121">**visTxtBlkLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="4eb32-121">**visTxtBlkLeftMargin**</span></span> <br/> |
   

