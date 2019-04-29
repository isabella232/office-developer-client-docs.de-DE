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
# <a name="width-cell-shape-transform-section"></a><span data-ttu-id="84b39-104">Zelle "Width" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="84b39-104">Width Cell (Shape Transform Section)</span></span>

<span data-ttu-id="84b39-105">Enthält die Breite des ausgewählten Shapes in Zeichnungseinheiten.</span><span class="sxs-lookup"><span data-stu-id="84b39-105">Contains the width of the selected shape in drawing units.</span></span> <span data-ttu-id="84b39-106">Die Standardformel zur Bestimmung der Breite eines 1D-Shapes lautet:</span><span class="sxs-lookup"><span data-stu-id="84b39-106">The default formula for determining the width of a 1-D shape is:</span></span>
  
<span data-ttu-id="84b39-107">= SQRT((EndeX - AnfangX) ^ 2 + (EndeY - AnfangY) ^ 2)</span><span class="sxs-lookup"><span data-stu-id="84b39-107">= SQRT((EndX - BeginX) ^ 2 + (EndY - BeginY) ^ 2)</span></span>
  
## <a name="remarks"></a><span data-ttu-id="84b39-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84b39-108">Remarks</span></span>

<span data-ttu-id="84b39-109">Wenn Sie einen Verweis auf die Zelle Width aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="84b39-109">To get a reference to the Width cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84b39-110">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="84b39-110">Cell name:</span></span>  <br/> | <span data-ttu-id="84b39-111">Width</span><span class="sxs-lookup"><span data-stu-id="84b39-111">Width</span></span>  <br/> |
   
<span data-ttu-id="84b39-112">Wenn Sie einen Verweis auf die Zelle "width" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="84b39-112">To get a reference to the Width cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="84b39-113">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="84b39-113">Section index:</span></span>  <br/> |<span data-ttu-id="84b39-114">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="84b39-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="84b39-115">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="84b39-115">Row index:</span></span>  <br/> |<span data-ttu-id="84b39-116">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="84b39-116">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="84b39-117">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="84b39-117">Cell index:</span></span>  <br/> |<span data-ttu-id="84b39-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="84b39-118">**visXFormWidth**</span></span> <br/> |
   

