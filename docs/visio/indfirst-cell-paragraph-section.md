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
ms.openlocfilehash: aa6d9fd14a40f4fe6b269d9750f603d8faf1d550
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335357"
---
# <a name="indfirst-cell-paragraph-section"></a><span data-ttu-id="ef607-105">Zelle "IndFirst" (Abschnitt "Paragraph")</span><span class="sxs-lookup"><span data-stu-id="ef607-105">IndFirst Cell (Paragraph Section)</span></span>

<span data-ttu-id="ef607-p102">Stellt den Abstand dar, den die erste Zeile jedes einzelnen Absatzes im Textblock des Shapes vom linken Einzug des Absatzes eingezogen ist. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der Einzug der ersten Zeile gleich.</span><span class="sxs-lookup"><span data-stu-id="ef607-p102">Represents the distance the first line of each paragraph in the shape's text block is indented from the left indent of the paragraph. This value is independent of the scale of the drawing. If the drawing is scaled, the first line indent remains the same.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ef607-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ef607-109">Remarks</span></span>

<span data-ttu-id="ef607-110">Wenn Sie einen Verweis auf die Zelle IndFirst aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ef607-110">To get a reference to the IndFirst cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ef607-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ef607-111">Cell name:</span></span>  <br/> | <span data-ttu-id="ef607-112">Abs. IndFirst [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ef607-112">Para.IndFirst[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ef607-113">Wenn Sie einen Verweis auf die Zelle IndFirst aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ef607-113">To get a reference to the IndFirst cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ef607-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ef607-114">Section index:</span></span>  <br/> |<span data-ttu-id="ef607-115">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="ef607-115">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="ef607-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ef607-116">Row index:</span></span>  <br/> |<span data-ttu-id="ef607-117">**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ef607-117">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ef607-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ef607-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ef607-119">**visIndentFirst**</span><span class="sxs-lookup"><span data-stu-id="ef607-119">**visIndentFirst**</span></span> <br/> |
   

