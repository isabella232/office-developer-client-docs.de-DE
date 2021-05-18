---
title: Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404771"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="ffeff-103">Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="ffeff-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ffeff-104">Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.</span><span class="sxs-lookup"><span data-stu-id="ffeff-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="ffeff-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ffeff-105">**Value**</span></span>|<span data-ttu-id="ffeff-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="ffeff-106">**Line Jump Direction**</span></span>|<span data-ttu-id="ffeff-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="ffeff-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ffeff-108">0</span><span class="sxs-lookup"><span data-stu-id="ffeff-108">0</span></span>  <br/> | <span data-ttu-id="ffeff-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="ffeff-109">Page default</span></span>  <br/> |<span data-ttu-id="ffeff-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="ffeff-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="ffeff-111">1</span><span class="sxs-lookup"><span data-stu-id="ffeff-111">1</span></span>  <br/> | <span data-ttu-id="ffeff-112">Nach links</span><span class="sxs-lookup"><span data-stu-id="ffeff-112">Left</span></span>  <br/> |<span data-ttu-id="ffeff-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="ffeff-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="ffeff-114">2</span><span class="sxs-lookup"><span data-stu-id="ffeff-114">2</span></span>  <br/> | <span data-ttu-id="ffeff-115">Nach rechts</span><span class="sxs-lookup"><span data-stu-id="ffeff-115">Right</span></span>  <br/> |<span data-ttu-id="ffeff-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="ffeff-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffeff-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ffeff-117">Remarks</span></span>

<span data-ttu-id="ffeff-118">Verwenden Sie die Zelle  PageLineJumpDirY im Abschnitt Seitenlayout, um die standardmäßige vertikale Richtung für alle Verbindersprünge auf einer Seite zu festlegen.</span><span class="sxs-lookup"><span data-stu-id="ffeff-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="ffeff-119">Um einen Verweis auf die Zelle ConLineJumpDirY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="ffeff-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ffeff-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ffeff-120">Cell name:</span></span>  <br/> | <span data-ttu-id="ffeff-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="ffeff-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="ffeff-122">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ConLineJumpDirY-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="ffeff-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ffeff-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ffeff-123">Section index:</span></span>  <br/> |<span data-ttu-id="ffeff-124">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ffeff-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ffeff-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ffeff-125">Row index:</span></span>  <br/> |<span data-ttu-id="ffeff-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ffeff-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="ffeff-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ffeff-127">Cell index:</span></span>  <br/> |<span data-ttu-id="ffeff-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="ffeff-128">**visSLOJumpDirY**</span></span> <br/> |
   

