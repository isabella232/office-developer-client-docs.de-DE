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
ms.openlocfilehash: 544557f1e797315619bc9975db0b87a09981726c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417210"
---
# <a name="bottommargin-cell-text-block-format-section"></a><span data-ttu-id="39e65-106">Zelle "BottomMargin" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="39e65-106">BottomMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="39e65-p102">Bestimmt den Abstand zwischen dem unteren Rand des Textblocks und der letzten darin enthaltenen Textzeile. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Größe der Zeichnung verändert wird, bleibt der untere Rand gleich.</span><span class="sxs-lookup"><span data-stu-id="39e65-p102">Determines the distance between the bottom border of the text block and the last line of text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the bottom margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="39e65-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="39e65-111">Remarks</span></span>

<span data-ttu-id="39e65-112">Wenn Sie einen Verweis auf die Zelle BottomMargin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="39e65-112">To get a reference to the BottomMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="39e65-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="39e65-113">Cell name:</span></span>  <br/> | <span data-ttu-id="39e65-114">BottomMargin</span><span class="sxs-lookup"><span data-stu-id="39e65-114">BottomMargin</span></span>  <br/> |
   
<span data-ttu-id="39e65-115">Wenn Sie einen Verweis auf die Zelle BottomMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="39e65-115">To get a reference to the BottomMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="39e65-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="39e65-116">Section index:</span></span>  <br/> |<span data-ttu-id="39e65-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="39e65-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="39e65-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="39e65-118">Row index:</span></span>  <br/> |<span data-ttu-id="39e65-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="39e65-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="39e65-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="39e65-120">Cell index:</span></span>  <br/> |<span data-ttu-id="39e65-121">**visTxtBlkBottomMargin**</span><span class="sxs-lookup"><span data-stu-id="39e65-121">**visTxtBlkBottomMargin**</span></span> <br/> |
   

