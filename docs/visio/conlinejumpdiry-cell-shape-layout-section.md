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
ms.openlocfilehash: 2d0c0964b52c9afbccc9cb507024825434702b6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796692"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a><span data-ttu-id="02868-103">ConLineJumpDirY Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="02868-103">ConLineJumpDirY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="02868-104">Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.</span><span class="sxs-lookup"><span data-stu-id="02868-104">Determines the line jump direction for line jumps occurring on a vertical dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="02868-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="02868-105">**Value**</span></span>|<span data-ttu-id="02868-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="02868-106">**Line Jump Direction**</span></span>|<span data-ttu-id="02868-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="02868-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="02868-108">0</span><span class="sxs-lookup"><span data-stu-id="02868-108">0</span></span>  <br/> | <span data-ttu-id="02868-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="02868-109">Page default</span></span>  <br/> |<span data-ttu-id="02868-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="02868-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="02868-111">1</span><span class="sxs-lookup"><span data-stu-id="02868-111">1</span></span>  <br/> | <span data-ttu-id="02868-112">Nach links</span><span class="sxs-lookup"><span data-stu-id="02868-112">Left</span></span>  <br/> |<span data-ttu-id="02868-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="02868-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="02868-114">2</span><span class="sxs-lookup"><span data-stu-id="02868-114">2</span></span>  <br/> | <span data-ttu-id="02868-115">Nach rechts</span><span class="sxs-lookup"><span data-stu-id="02868-115">Right</span></span>  <br/> |<span data-ttu-id="02868-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="02868-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02868-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="02868-117">Remarks</span></span>

<span data-ttu-id="02868-118">Zum Festlegen der vertikaler Richtung für *Alle* Verbinder auf einem Zeichenblatt springt, verwenden Sie die Zelle PageLineJumpDirY im Abschnitt Page Layout.</span><span class="sxs-lookup"><span data-stu-id="02868-118">To set the default vertical direction for  *all*  connector jumps on a page, use the PageLineJumpDirY cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="02868-119">Wenn Sie einen Verweis auf die Zelle ConLineJumpDirY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="02868-119">To get a reference to the ConLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02868-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="02868-120">Cell name:</span></span>  <br/> | <span data-ttu-id="02868-121">ConLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="02868-121">ConLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="02868-122">Wenn Sie einen Verweis auf die Zelle ConLineJumpDirY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="02868-122">To get a reference to the ConLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02868-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="02868-123">Section index:</span></span>  <br/> |<span data-ttu-id="02868-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="02868-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="02868-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="02868-125">Row index:</span></span>  <br/> |<span data-ttu-id="02868-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="02868-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="02868-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="02868-127">Cell index:</span></span>  <br/> |<span data-ttu-id="02868-128">**visSLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="02868-128">**visSLOJumpDirY**</span></span> <br/> |
   

