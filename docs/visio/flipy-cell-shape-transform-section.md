---
title: Zelle "FlipY" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251198
localization_priority: Normal
ms.assetid: 062022ff-e243-2540-becd-d9b969ce83ce
description: Gibt an, ob das Shape vertikal gekippt wurde.
ms.openlocfilehash: 44ea0341cda3655e8acc69e82e89acddac69b80d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346200"
---
# <a name="flipy-cell-shape-transform-section"></a><span data-ttu-id="a1f48-103">Zelle "FlipY" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="a1f48-103">FlipY Cell (Shape Transform Section)</span></span>

<span data-ttu-id="a1f48-104">Gibt an, ob das Shape vertikal gekippt wurde.</span><span class="sxs-lookup"><span data-stu-id="a1f48-104">Indicates whether the shape has been flipped vertically.</span></span>
  
|<span data-ttu-id="a1f48-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a1f48-105">**Value**</span></span>|<span data-ttu-id="a1f48-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1f48-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="a1f48-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="a1f48-107">TRUE</span></span>  <br/> | <span data-ttu-id="a1f48-108">Das Shape wurde vertikal gekippt.</span><span class="sxs-lookup"><span data-stu-id="a1f48-108">The shape has been flipped vertically.</span></span>  <br/> |
| <span data-ttu-id="a1f48-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="a1f48-109">FALSE</span></span>  <br/> | <span data-ttu-id="a1f48-110">Das Shape wurde nicht vertikal gekippt.</span><span class="sxs-lookup"><span data-stu-id="a1f48-110">The shape has not been flipped vertically.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1f48-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1f48-111">Remarks</span></span>

<span data-ttu-id="a1f48-112">Wenn Sie einen Verweis auf die Zelle FlipY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a1f48-112">To get a reference to the FlipY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1f48-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a1f48-113">Cell name:</span></span>  <br/> | <span data-ttu-id="a1f48-114">FlipY</span><span class="sxs-lookup"><span data-stu-id="a1f48-114">FlipY</span></span>  <br/> |
   
<span data-ttu-id="a1f48-115">Wenn Sie einen Verweis auf die Zelle FlipY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a1f48-115">To get a reference to the FlipY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a1f48-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a1f48-116">Section index:</span></span>  <br/> |<span data-ttu-id="a1f48-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a1f48-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a1f48-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a1f48-118">Row index:</span></span>  <br/> |<span data-ttu-id="a1f48-119">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="a1f48-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="a1f48-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a1f48-120">Cell index:</span></span>  <br/> |<span data-ttu-id="a1f48-121">**visXFormFlipY**</span><span class="sxs-lookup"><span data-stu-id="a1f48-121">**visXFormFlipY**</span></span> <br/> |
   

