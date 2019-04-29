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
ms.openlocfilehash: 97d349fd4ddc3c76cda61e1ee7ce25909161e6fa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435572"
---
# <a name="topmargin-cell-text-block-format-section"></a><span data-ttu-id="60f13-106">Zelle "TopMargin" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="60f13-106">TopMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="60f13-p102">Bestimmt den Abstand zwischen dem oberen Rand des Textblocks und der ersten darin enthaltenen Textzeile. Der Standardwert beträgt 4,0000 Punkt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der obere Rand unverändert.</span><span class="sxs-lookup"><span data-stu-id="60f13-p102">Determines the distance between the top border of the text block and the first line of text it contains. The default is 4.0000 point. This value is independent of the scale of the drawing. If the drawing is scaled, the top margin remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="60f13-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="60f13-111">Remarks</span></span>

<span data-ttu-id="60f13-112">Wenn Sie einen Verweis auf die Zelle oberRand aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="60f13-112">To get a reference to the TopMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60f13-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="60f13-113">Cell name:</span></span>  <br/> | <span data-ttu-id="60f13-114">TopMargin</span><span class="sxs-lookup"><span data-stu-id="60f13-114">TopMargin</span></span>  <br/> |
   
<span data-ttu-id="60f13-115">Wenn Sie einen Verweis auf die Zelle oberRand aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="60f13-115">To get a reference to the TopMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60f13-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="60f13-116">Section index:</span></span>  <br/> |<span data-ttu-id="60f13-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="60f13-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="60f13-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="60f13-118">Row index:</span></span>  <br/> |<span data-ttu-id="60f13-119">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="60f13-119">**visRowText**</span></span> <br/> |
| <span data-ttu-id="60f13-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="60f13-120">Cell index:</span></span>  <br/> |<span data-ttu-id="60f13-121">**visTxtBlkTopMargin**</span><span class="sxs-lookup"><span data-stu-id="60f13-121">**visTxtBlkTopMargin**</span></span> <br/> |
   

