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
ms.openlocfilehash: 55e77c5ccfca2425a8a2985564448e0f656aebbf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798409"
---
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="82b7f-104">Width Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="82b7f-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="82b7f-p102">Enthält die Breite des ausgewählten Shapes in Zeichnungseinheiten. Die Standardformel zur Bestimmung der Breite eines 1D-Shapes lautet:</span><span class="sxs-lookup"><span data-stu-id="82b7f-p102">Contains the width of the selected shape in drawing units. The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="82b7f-107">= SQRT((EndeX - AnfangX) ^ 2 + (EndeY - AnfangY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="82b7f-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82b7f-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="82b7f-108">Remarks</span></span>

<span data-ttu-id="82b7f-109">Wenn Sie einen Verweis auf die Zelle Width aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="82b7f-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="82b7f-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="82b7f-110">Cell name:</span></span>  <br/> | <span data-ttu-id="82b7f-111">Width</span><span class="sxs-lookup"><span data-stu-id="82b7f-111">Width</span></span>  <br/> |
   
<span data-ttu-id="82b7f-112">Wenn Sie einen Verweis auf die Zelle Width aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="82b7f-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="82b7f-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="82b7f-113">Section index:</span></span>  <br/> |<span data-ttu-id="82b7f-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="82b7f-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="82b7f-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="82b7f-115">Row index:</span></span>  <br/> |<span data-ttu-id="82b7f-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="82b7f-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="82b7f-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="82b7f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="82b7f-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="82b7f-118">**visXFormWidth**</span></span> <br/> |
   

