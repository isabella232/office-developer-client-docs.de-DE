---
title: Zelle "FlipX" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: Gibt an, ob das Shape horizontal gekippt wurde.
ms.openlocfilehash: b7a4a15e5a7759eddcda3ec391a81f14df545691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415950"
---
# <a name="flipx-cell-shape-transform-section"></a><span data-ttu-id="ca44a-103">Zelle "FlipX" (Abschnitt "Shape Transform")</span><span class="sxs-lookup"><span data-stu-id="ca44a-103">FlipX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="ca44a-104">Gibt an, ob das Shape horizontal gekippt wurde.</span><span class="sxs-lookup"><span data-stu-id="ca44a-104">Indicates whether the shape has been flipped horizontally.</span></span>
  
|<span data-ttu-id="ca44a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ca44a-105">**Value**</span></span>|<span data-ttu-id="ca44a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca44a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ca44a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ca44a-107">TRUE</span></span>  <br/> | <span data-ttu-id="ca44a-108">Das Shape wurde horizontal gekippt.</span><span class="sxs-lookup"><span data-stu-id="ca44a-108">The shape has been flipped horizontally.</span></span>  <br/> |
| <span data-ttu-id="ca44a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ca44a-109">FALSE</span></span>  <br/> | <span data-ttu-id="ca44a-110">Das Shape wurde nicht horizontal gekippt.</span><span class="sxs-lookup"><span data-stu-id="ca44a-110">The shape has not been flipped horizontally.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca44a-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ca44a-111">Remarks</span></span>

<span data-ttu-id="ca44a-112">Verwenden Sie zum Erhalten eines Verweises auf die Zelle FlipX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="ca44a-112">To get a reference to the FlipX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca44a-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ca44a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ca44a-114">FlipX</span><span class="sxs-lookup"><span data-stu-id="ca44a-114">FlipX</span></span>  <br/> |
   
<span data-ttu-id="ca44a-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die FlipX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="ca44a-115">To get a reference to the FlipX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca44a-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ca44a-116">Section index:</span></span>  <br/> |<span data-ttu-id="ca44a-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca44a-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ca44a-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ca44a-118">Row index:</span></span>  <br/> |<span data-ttu-id="ca44a-119">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="ca44a-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="ca44a-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ca44a-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ca44a-121">**visXFormFlipX**</span><span class="sxs-lookup"><span data-stu-id="ca44a-121">**visXFormFlipX**</span></span> <br/> |
   

