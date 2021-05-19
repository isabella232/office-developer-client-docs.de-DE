---
title: Zelle "Width" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251194
localization_priority: Normal
ms.assetid: 992ae9d8-ea15-0f5c-ccd6-e4c536099692
description: 'Enthält die Breite des ausgewählten Shapes in Zeichnungseinheiten. Die Standardformel zur Bestimmung der Breite eines 1D-Shapes lautet:'
ms.openlocfilehash: c99f4669f3b27390a5b8e9062d6085a5a9db54e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415194"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="83ee2-104">Zelle "Width" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="83ee2-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="83ee2-p102">Enthält die Breite des ausgewählten Shapes in Zeichnungseinheiten. Die Standardformel zur Bestimmung der Breite eines 1D-Shapes lautet:</span><span class="sxs-lookup"><span data-stu-id="83ee2-p102">Contains the width of the selected shape in drawing units. The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="83ee2-107">= SQRT((EndeX - AnfangX) ^ 2 + (EndeY - AnfangY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="83ee2-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="83ee2-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="83ee2-108">Remarks</span></span>

<span data-ttu-id="83ee2-109">Um einen Verweis auf die Zelle Width anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="83ee2-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83ee2-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="83ee2-110">Cell name:</span></span>  <br/> | <span data-ttu-id="83ee2-111">Width</span><span class="sxs-lookup"><span data-stu-id="83ee2-111">Width</span></span>  <br/> |
   
<span data-ttu-id="83ee2-112">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Width nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="83ee2-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="83ee2-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="83ee2-113">Section index:</span></span>  <br/> |<span data-ttu-id="83ee2-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="83ee2-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="83ee2-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="83ee2-115">Row index:</span></span>  <br/> |<span data-ttu-id="83ee2-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="83ee2-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="83ee2-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="83ee2-117">Cell index:</span></span>  <br/> |<span data-ttu-id="83ee2-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="83ee2-118">**visXFormWidth**</span></span> <br/> |
   

