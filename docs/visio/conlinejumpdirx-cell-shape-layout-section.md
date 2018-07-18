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
# <a name="conlinejumpdirx-cell-shape-layout-section"></a><span data-ttu-id="25ff7-103">ConLineJumpDirX Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="25ff7-103">ConLineJumpDirX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="25ff7-104">Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.</span><span class="sxs-lookup"><span data-stu-id="25ff7-104">Determines the line jump direction for line jumps occurring on a horizontal dynamic connector for a shape.</span></span>
  
|<span data-ttu-id="25ff7-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="25ff7-105">**Value**</span></span>|<span data-ttu-id="25ff7-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="25ff7-106">**Line jump direction**</span></span>|<span data-ttu-id="25ff7-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="25ff7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="25ff7-108">0</span><span class="sxs-lookup"><span data-stu-id="25ff7-108">0</span></span>  <br/> | <span data-ttu-id="25ff7-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="25ff7-109">Page default</span></span>  <br/> |<span data-ttu-id="25ff7-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="25ff7-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="25ff7-111">1</span><span class="sxs-lookup"><span data-stu-id="25ff7-111">1</span></span>  <br/> | <span data-ttu-id="25ff7-112">Nach oben</span><span class="sxs-lookup"><span data-stu-id="25ff7-112">Up</span></span>  <br/> |<span data-ttu-id="25ff7-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="25ff7-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="25ff7-114">2</span><span class="sxs-lookup"><span data-stu-id="25ff7-114">2</span></span>  <br/> | <span data-ttu-id="25ff7-115">Nach unten</span><span class="sxs-lookup"><span data-stu-id="25ff7-115">Down</span></span>  <br/> |<span data-ttu-id="25ff7-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="25ff7-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25ff7-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="25ff7-117">Remarks</span></span>

<span data-ttu-id="25ff7-118">Zum Festlegen der horizontaler Richtung für *Alle* Verbinder auf einem Zeichenblatt springt, verwenden Sie die Zelle PageLineJumpDirX im Abschnitt Page Layout.</span><span class="sxs-lookup"><span data-stu-id="25ff7-118">To set the default horizontal direction for  *all*  connector jumps on a page, use the PageLineJumpDirX cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="25ff7-119">Wenn Sie einen Verweis auf die Zelle ConLineJumpDirX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="25ff7-119">To get a reference to the ConLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25ff7-120">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="25ff7-120">Cell name:</span></span>  <br/> | <span data-ttu-id="25ff7-121">ConLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="25ff7-121">ConLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="25ff7-122">Wenn Sie einen Verweis auf die Zelle ConLineJumpDirX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="25ff7-122">To get a reference to the ConLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="25ff7-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="25ff7-123">Section index:</span></span>  <br/> |<span data-ttu-id="25ff7-124">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="25ff7-124">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="25ff7-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="25ff7-125">Row index:</span></span>  <br/> |<span data-ttu-id="25ff7-126">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="25ff7-126">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="25ff7-127">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="25ff7-127">Cell index:</span></span>  <br/> |<span data-ttu-id="25ff7-128">**visSLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="25ff7-128">**visSLOJumpDirX**</span></span> <br/> |
   

