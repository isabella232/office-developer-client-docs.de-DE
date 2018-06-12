---
title: Zelle "IndFirst" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Stellt den Abstand dar, den die erste Zeile jedes einzelnen Absatzes im Textblock des Shapes vom linken Einzug des Absatzes eingezogen ist. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der Einzug der ersten Zeile gleich.
ms.openlocfilehash: 03c34a0ccd1681d3523d743ebfc34af7b9dcfa87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797192"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="8cf4d-105">Zelle "IndFirst" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="8cf4d-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="8cf4d-p102">Stellt den Abstand dar, den die erste Zeile jedes einzelnen Absatzes im Textblock des Shapes vom linken Einzug des Absatzes eingezogen ist. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der Einzug der ersten Zeile gleich.</span><span class="sxs-lookup"><span data-stu-id="8cf4d-p102">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph. This value is independent of the scale of the drawing. If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8cf4d-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8cf4d-109">Remarks</span></span>

<span data-ttu-id="8cf4d-110">Wenn Sie einen Verweis auf die Zelle IndFirst nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8cf4d-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8cf4d-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8cf4d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="8cf4d-112">Para.IndFirst [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="8cf4d-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="8cf4d-113">Wenn Sie einen Verweis auf die Zelle IndFirst aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8cf4d-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8cf4d-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8cf4d-114">Section index:</span></span>  <br/> |<span data-ttu-id="8cf4d-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="8cf4d-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="8cf4d-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8cf4d-116">Row index:</span></span>  <br/> |<span data-ttu-id="8cf4d-117">**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="8cf4d-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="8cf4d-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8cf4d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="8cf4d-119">**visIndentFirst**</span><span class="sxs-lookup"><span data-stu-id="8cf4d-119">**visIndentFirst**</span></span> <br/> |
   

