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
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="41b8c-103">Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="41b8c-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="41b8c-104">Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.</span><span class="sxs-lookup"><span data-stu-id="41b8c-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="41b8c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="41b8c-105">**Value**</span></span>|<span data-ttu-id="41b8c-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="41b8c-106">**Line Jump Direction**</span></span>|<span data-ttu-id="41b8c-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="41b8c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="41b8c-108">0</span><span class="sxs-lookup"><span data-stu-id="41b8c-108">0</span></span>  <br/> | <span data-ttu-id="41b8c-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="41b8c-109">Page default</span></span>  <br/> |<span data-ttu-id="41b8c-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="41b8c-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="41b8c-111">1</span><span class="sxs-lookup"><span data-stu-id="41b8c-111">1</span></span>  <br/> | <span data-ttu-id="41b8c-112">Nach links</span><span class="sxs-lookup"><span data-stu-id="41b8c-112">Left</span></span>  <br/> |<span data-ttu-id="41b8c-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="41b8c-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="41b8c-114">2</span><span class="sxs-lookup"><span data-stu-id="41b8c-114">2</span></span>  <br/> | <span data-ttu-id="41b8c-115">Nach rechts</span><span class="sxs-lookup"><span data-stu-id="41b8c-115">Right</span></span>  <br/> |<span data-ttu-id="41b8c-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="41b8c-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41b8c-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41b8c-117">Remarks</span></span>

<span data-ttu-id="41b8c-118">Wenn Sie die standardmäßige vertikale Richtung für *alle* Verbinder-Sprünge auf einer Seite festlegen möchten, verwenden Sie die Zelle Zelle PageLineJumpDirY im Abschnitt Seiten Layout.</span><span class="sxs-lookup"><span data-stu-id="41b8c-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="41b8c-119">Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpDirY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="41b8c-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41b8c-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="41b8c-120">Cell name:</span></span>  <br/> | <span data-ttu-id="41b8c-121">Zelle ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="41b8c-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="41b8c-122">Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpDirY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="41b8c-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="41b8c-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="41b8c-123">Section index:</span></span>  <br/> |<span data-ttu-id="41b8c-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="41b8c-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="41b8c-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="41b8c-125">Row index:</span></span>  <br/> |<span data-ttu-id="41b8c-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="41b8c-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="41b8c-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="41b8c-127">Cell index:</span></span>  <br/> |<span data-ttu-id="41b8c-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="41b8c-128">**visSLOJumpDirY**</span></span> <br/> |
   

