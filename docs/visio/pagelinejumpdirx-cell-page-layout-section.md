---
title: Zelle "PageLineJumpDirX" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251656
localization_priority: Normal
ms.assetid: 77892ec7-4c6a-78a5-5af4-5b6be7709e77
description: Bestimmt die Richtung von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.
ms.openlocfilehash: 4e1213990877e1260cc8cecd5a55beda4592a844
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431008"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="0b6b0-103">Zelle "PageLineJumpDirX" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="0b6b0-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="0b6b0-104">Bestimmt die Richtung von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="0b6b0-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="0b6b0-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-105">**Value**</span></span>|<span data-ttu-id="0b6b0-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-106">**Line jump direction**</span></span>|<span data-ttu-id="0b6b0-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0b6b0-108">0</span><span class="sxs-lookup"><span data-stu-id="0b6b0-108">0</span></span>  <br/> | <span data-ttu-id="0b6b0-109">Standard, nach links oder die Einstellung des Zeichenblatts für Shapes</span><span class="sxs-lookup"><span data-stu-id="0b6b0-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="0b6b0-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="0b6b0-111">1</span><span class="sxs-lookup"><span data-stu-id="0b6b0-111">1</span></span>  <br/> | <span data-ttu-id="0b6b0-112">Nach oben</span><span class="sxs-lookup"><span data-stu-id="0b6b0-112">Up</span></span>  <br/> |<span data-ttu-id="0b6b0-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="0b6b0-114">2</span><span class="sxs-lookup"><span data-stu-id="0b6b0-114">2</span></span>  <br/> | <span data-ttu-id="0b6b0-115">Nach unten</span><span class="sxs-lookup"><span data-stu-id="0b6b0-115">Down</span></span>  <br/> |<span data-ttu-id="0b6b0-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0b6b0-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0b6b0-117">Remarks</span></span>

<span data-ttu-id="0b6b0-118">Um einen Verweis auf die Zelle PageLineJumpDirX anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="0b6b0-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0b6b0-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0b6b0-119">Cell name:</span></span>  <br/> | <span data-ttu-id="0b6b0-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="0b6b0-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="0b6b0-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die PageLineJumpDirX-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="0b6b0-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0b6b0-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0b6b0-122">Section index:</span></span>  <br/> |<span data-ttu-id="0b6b0-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0b6b0-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0b6b0-124">Row index:</span></span>  <br/> |<span data-ttu-id="0b6b0-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="0b6b0-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0b6b0-126">Cell index:</span></span>  <br/> |<span data-ttu-id="0b6b0-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="0b6b0-127">**visPLOJumpDirX**</span></span> <br/> |
   

