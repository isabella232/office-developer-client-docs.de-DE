---
title: Zelle "BottomMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm120
localization_priority: Normal
ms.assetid: 3121911b-34d5-d99c-3806-76f6e2824f92
description: Bestimmt den Abstand zwischen dem unteren Rand des Textblocks und der letzten darin enthaltenen Textzeile. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Größe der Zeichnung verändert wird, bleibt der untere Rand gleich.
ms.openlocfilehash: f3515485b0418ffeaf55910a972e1e480f428e4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796547"
---
# <a name="bottommargin-cell-text-block-format-section"></a><span data-ttu-id="67031-106">BottomMargin Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="67031-106">BottomMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="67031-p102">Bestimmt den Abstand zwischen dem unteren Rand des Textblocks und der letzten darin enthaltenen Textzeile. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Größe der Zeichnung verändert wird, bleibt der untere Rand gleich.</span><span class="sxs-lookup"><span data-stu-id="67031-p102">Determines the distance between the bottom border of the text block and the last line of text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the bottom margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67031-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="67031-111">Remarks</span></span>

<span data-ttu-id="67031-112">Wenn Sie einen Verweis auf die Zelle BottomMargin aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="67031-112">To get a reference to the BottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67031-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="67031-113">Cell name:</span></span>  <br/> | <span data-ttu-id="67031-114">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="67031-114">BottomMargin</span></span>  <br/> |
   
<span data-ttu-id="67031-115">Wenn Sie einen Verweis auf die Zelle BottomMargin aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="67031-115">To get a reference to the BottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67031-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="67031-116">Section index:</span></span>  <br/> |<span data-ttu-id="67031-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="67031-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="67031-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="67031-118">Row index:</span></span>  <br/> |<span data-ttu-id="67031-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="67031-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="67031-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="67031-120">Cell index:</span></span>  <br/> |<span data-ttu-id="67031-121">**visTxtBlkBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="67031-121">**visTxtBlkBottomMargin**</span></span> <br/> |
   

