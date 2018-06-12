---
title: Zelle "RightMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Bestimmt den Abstand zwischen dem rechten Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt.
ms.openlocfilehash: 57fdb320395a9a6562983a0148b37c4a70a9a9b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797859"
---
# <a name="rightmargin-cell-text-block-format-section"></a><span data-ttu-id="338dd-104">Zelle "RightMargin" (Abschnitt "Text Block Format")</span><span class="sxs-lookup"><span data-stu-id="338dd-104">RightMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="338dd-p102">Bestimmt den Abstand zwischen dem rechten Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt.</span><span class="sxs-lookup"><span data-stu-id="338dd-p102">Determines the distance between the right border of the text block and the text it contains. The default is 0.1 inch.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="338dd-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="338dd-107">Remarks</span></span>

<span data-ttu-id="338dd-p103">Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der rechte Rand unverändert.</span><span class="sxs-lookup"><span data-stu-id="338dd-p103">This value is independent of the scale of the drawing. If the drawing is scaled, the right margin remains the same.</span></span>
  
<span data-ttu-id="338dd-110">Wenn Sie einen Verweis auf die Zelle RightMargin nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="338dd-110">To get a reference to the RightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="338dd-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="338dd-111">Cell name:</span></span>  <br/> | <span data-ttu-id="338dd-112">RightMargin</span><span class="sxs-lookup"><span data-stu-id="338dd-112">RightMargin</span></span>  <br/> |
   
<span data-ttu-id="338dd-113">Wenn Sie einen Verweis auf die Zelle RightMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="338dd-113">To get a reference to the RightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="338dd-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="338dd-114">Section index:</span></span>  <br/> |<span data-ttu-id="338dd-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="338dd-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="338dd-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="338dd-116">Row index:</span></span>  <br/> |<span data-ttu-id="338dd-117">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="338dd-117">**visRowText**</span></span> <br/> |
| <span data-ttu-id="338dd-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="338dd-118">Cell index:</span></span>  <br/> |<span data-ttu-id="338dd-119">**visTxtBlkRightMargin**</span><span class="sxs-lookup"><span data-stu-id="338dd-119">**visTxtBlkRightMargin**</span></span> <br/> |
   

