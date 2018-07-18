---
title: Zelle "TopMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1015
localization_priority: Normal
ms.assetid: c599b444-4d0e-a855-b04b-dd9dcaedf263
description: Bestimmt den Abstand zwischen dem oberen Rand des Textblocks und der ersten darin enthaltenen Textzeile. Der Standardwert beträgt 4,0000 Punkt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der obere Rand unverändert.
ms.openlocfilehash: 71e8e3b41dc9c59c374111dcd442e55ab70330fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798307"
---
# <a name="topmargin-cell-text-block-format-section"></a><span data-ttu-id="00579-106">TopMargin Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="00579-106">TopMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="00579-p102">Bestimmt den Abstand zwischen dem oberen Rand des Textblocks und der ersten darin enthaltenen Textzeile. Der Standardwert beträgt 4,0000 Punkt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der obere Rand unverändert.</span><span class="sxs-lookup"><span data-stu-id="00579-p102">Determines the distance between the top border of the text block and the first line of text it contains. The default is 4.0000 point. This value is independent of the scale of the drawing. If the drawing is scaled, the top margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00579-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00579-111">Remarks</span></span>

<span data-ttu-id="00579-112">Wenn Sie einen Verweis auf die Zelle TopMargin aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="00579-112">To get a reference to the TopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00579-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="00579-113">Cell name:</span></span>  <br/> | <span data-ttu-id="00579-114">TopMargin</span><span class="sxs-lookup"><span data-stu-id="00579-114">TopMargin</span></span>  <br/> |
   
<span data-ttu-id="00579-115">Wenn Sie einen Verweis auf die Zelle TopMargin aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="00579-115">To get a reference to the TopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="00579-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="00579-116">Section index:</span></span>  <br/> |<span data-ttu-id="00579-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="00579-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="00579-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="00579-118">Row index:</span></span>  <br/> |<span data-ttu-id="00579-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="00579-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="00579-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="00579-120">Cell index:</span></span>  <br/> |<span data-ttu-id="00579-121">**visTxtBlkTopMargin**</span><span class="sxs-lookup"><span data-stu-id="00579-121">**visTxtBlkTopMargin**</span></span> <br/> |
   

