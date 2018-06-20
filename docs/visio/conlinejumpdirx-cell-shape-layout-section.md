---
title: Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
localization_priority: Normal
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: 396830d0da22c15f036f95808b3a94c33e9dc5bb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796704"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="6a26e-103">Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="6a26e-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="6a26e-104">Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.</span><span class="sxs-lookup"><span data-stu-id="6a26e-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="6a26e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6a26e-105">**Value**</span></span>|<span data-ttu-id="6a26e-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="6a26e-106">**Line jump direction**</span></span>|<span data-ttu-id="6a26e-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="6a26e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6a26e-108">0</span><span class="sxs-lookup"><span data-stu-id="6a26e-108">0</span></span>  <br/> | <span data-ttu-id="6a26e-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="6a26e-109">Page default</span></span>  <br/> |<span data-ttu-id="6a26e-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="6a26e-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="6a26e-111">1</span><span class="sxs-lookup"><span data-stu-id="6a26e-111">1</span></span>  <br/> | <span data-ttu-id="6a26e-112">Nach oben</span><span class="sxs-lookup"><span data-stu-id="6a26e-112">Up</span></span>  <br/> |<span data-ttu-id="6a26e-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="6a26e-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="6a26e-114">2</span><span class="sxs-lookup"><span data-stu-id="6a26e-114">2</span></span>  <br/> | <span data-ttu-id="6a26e-115">Nach unten</span><span class="sxs-lookup"><span data-stu-id="6a26e-115">Down</span></span>  <br/> |<span data-ttu-id="6a26e-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="6a26e-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a26e-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a26e-117">Remarks</span></span>

<span data-ttu-id="6a26e-118">Zum Festlegen der horizontaler Richtung für *Alle* Verbinder auf einem Zeichenblatt springt, verwenden Sie die Zelle PageLineJumpDirX im Abschnitt Page Layout.</span><span class="sxs-lookup"><span data-stu-id="6a26e-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="6a26e-119">Wenn Sie einen Verweis auf die Zelle ConLineJumpDirX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6a26e-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a26e-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6a26e-120">Cell name:</span></span>  <br/> | <span data-ttu-id="6a26e-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="6a26e-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="6a26e-122">Wenn Sie einen Verweis auf die Zelle ConLineJumpDirX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6a26e-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a26e-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6a26e-123">Section index:</span></span>  <br/> |<span data-ttu-id="6a26e-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a26e-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a26e-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6a26e-125">Row index:</span></span>  <br/> |<span data-ttu-id="6a26e-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="6a26e-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="6a26e-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6a26e-127">Cell index:</span></span>  <br/> |<span data-ttu-id="6a26e-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="6a26e-128">**visSLOJumpDirX**</span></span> <br/> |
   

