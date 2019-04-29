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
# <a name="leftmargin-cell-text-block-format-section"></a><span data-ttu-id="bbf16-106">Zelle "LeftMargin" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="bbf16-106">LeftMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="bbf16-p102">Bestimmt den Abstand zwischen dem linken Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der linke Rand unverändert.</span><span class="sxs-lookup"><span data-stu-id="bbf16-p102">Determines the distance between the left border of the text block and the text it contains. The default is 0.1 inch. This value is independent of the scale of the drawing. If the drawing is scaled, the left margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bbf16-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bbf16-111">Remarks</span></span>

<span data-ttu-id="bbf16-112">Wenn Sie einen Verweis auf die Zelle LeftMargin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bbf16-112">To get a reference to the LeftMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bbf16-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bbf16-113">Cell name:</span></span>  <br/> | <span data-ttu-id="bbf16-114">LeftMargin</span><span class="sxs-lookup"><span data-stu-id="bbf16-114">LeftMargin</span></span>  <br/> |
   
<span data-ttu-id="bbf16-115">Wenn Sie einen Verweis auf die Zelle LeftMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bbf16-115">To get a reference to the LeftMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bbf16-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bbf16-116">Section index:</span></span>  <br/> |<span data-ttu-id="bbf16-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bbf16-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bbf16-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bbf16-118">Row index:</span></span>  <br/> |<span data-ttu-id="bbf16-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="bbf16-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="bbf16-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bbf16-120">Cell index:</span></span>  <br/> |<span data-ttu-id="bbf16-121">**visTxtBlkLeftMargin**</span><span class="sxs-lookup"><span data-stu-id="bbf16-121">**visTxtBlkLeftMargin**</span></span> <br/> |
   

