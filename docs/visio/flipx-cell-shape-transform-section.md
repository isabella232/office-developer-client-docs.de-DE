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
ms.openlocfilehash: fc014ff6c5a3650361d6afd478a5858f84fb5c47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797035"
---
# <a name="flipx-cell-shape-transform-section"></a><span data-ttu-id="40382-103">FlipX Cell (Shape Transform Section)</span><span class="sxs-lookup"><span data-stu-id="40382-103">FlipX Cell (Shape Transform Section)</span></span>

<span data-ttu-id="40382-104">Gibt an, ob das Shape horizontal gekippt wurde.</span><span class="sxs-lookup"><span data-stu-id="40382-104">Indicates whether the shape has been flipped horizontally.</span></span>
  
|<span data-ttu-id="40382-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="40382-105">**Value**</span></span>|<span data-ttu-id="40382-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40382-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="40382-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="40382-107">TRUE</span></span>  <br/> | <span data-ttu-id="40382-108">Das Shape wurde horizontal gekippt.</span><span class="sxs-lookup"><span data-stu-id="40382-108">The shape has been flipped horizontally.</span></span>  <br/> |
| <span data-ttu-id="40382-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="40382-109">FALSE</span></span>  <br/> | <span data-ttu-id="40382-110">Das Shape wurde nicht horizontal gekippt.</span><span class="sxs-lookup"><span data-stu-id="40382-110">The shape has not been flipped horizontally.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40382-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="40382-111">Remarks</span></span>

<span data-ttu-id="40382-112">Wenn Sie einen Verweis auf die Zelle FlipX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="40382-112">To get a reference to the FlipX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40382-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="40382-113">Cell name:</span></span>  <br/> | <span data-ttu-id="40382-114">FlipX</span><span class="sxs-lookup"><span data-stu-id="40382-114">FlipX</span></span>  <br/> |
   
<span data-ttu-id="40382-115">Wenn Sie einen Verweis auf die Zelle FlipX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="40382-115">To get a reference to the FlipX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="40382-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="40382-116">Section index:</span></span>  <br/> |<span data-ttu-id="40382-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="40382-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="40382-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="40382-118">Row index:</span></span>  <br/> |<span data-ttu-id="40382-119">**visRowXFormOut**</span><span class="sxs-lookup"><span data-stu-id="40382-119">**visRowXFormOut**</span></span> <br/> |
| <span data-ttu-id="40382-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="40382-120">Cell index:</span></span>  <br/> |<span data-ttu-id="40382-121">**visXFormFlipX**</span><span class="sxs-lookup"><span data-stu-id="40382-121">**visXFormFlipX**</span></span> <br/> |
   

