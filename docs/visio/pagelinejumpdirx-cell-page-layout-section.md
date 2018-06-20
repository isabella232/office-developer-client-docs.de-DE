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
ms.openlocfilehash: d414313e98107790f9236c0afabdc5747c6a2a10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797584"
---
# <a name="pagelinejumpdirx-cell-page-layout-section"></a><span data-ttu-id="6b41f-103">PageLineJumpDirX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="6b41f-103">PageLineJumpDirX Cell (Page Layout Section)</span></span>

<span data-ttu-id="6b41f-104">Bestimmt die Richtung von Liniensprüngen auf horizontalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="6b41f-104">Determines the direction of line jumps on horizontal dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="6b41f-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6b41f-105">**Value**</span></span>|<span data-ttu-id="6b41f-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="6b41f-106">**Line jump direction**</span></span>|<span data-ttu-id="6b41f-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="6b41f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6b41f-108">0</span><span class="sxs-lookup"><span data-stu-id="6b41f-108">0</span></span>  <br/> | <span data-ttu-id="6b41f-109">Standard, nach links oder die Einstellung des Zeichenblatts für Shapes</span><span class="sxs-lookup"><span data-stu-id="6b41f-109">Default; left or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="6b41f-110">**visLOJumpDirXDefault**</span><span class="sxs-lookup"><span data-stu-id="6b41f-110">**visLOJumpDirXDefault**</span></span> <br/> |
| <span data-ttu-id="6b41f-111">1</span><span class="sxs-lookup"><span data-stu-id="6b41f-111">1</span></span>  <br/> | <span data-ttu-id="6b41f-112">Nach oben</span><span class="sxs-lookup"><span data-stu-id="6b41f-112">Up</span></span>  <br/> |<span data-ttu-id="6b41f-113">**visLOJumpDirXUp**</span><span class="sxs-lookup"><span data-stu-id="6b41f-113">**visLOJumpDirXUp**</span></span> <br/> |
| <span data-ttu-id="6b41f-114">2</span><span class="sxs-lookup"><span data-stu-id="6b41f-114">2</span></span>  <br/> | <span data-ttu-id="6b41f-115">Nach unten</span><span class="sxs-lookup"><span data-stu-id="6b41f-115">Down</span></span>  <br/> |<span data-ttu-id="6b41f-116">**visLOJumpDirXDown**</span><span class="sxs-lookup"><span data-stu-id="6b41f-116">**visLOJumpDirXDown**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b41f-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6b41f-117">Remarks</span></span>

<span data-ttu-id="6b41f-118">Wenn Sie einen Verweis auf die Zelle PageLineJumpDirX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6b41f-118">To get a reference to the PageLineJumpDirX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b41f-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6b41f-119">Cell name:</span></span>  <br/> | <span data-ttu-id="6b41f-120">PageLineJumpDirX</span><span class="sxs-lookup"><span data-stu-id="6b41f-120">PageLineJumpDirX</span></span>  <br/> |
   
<span data-ttu-id="6b41f-121">Wenn Sie einen Verweis auf die Zelle PageLineJumpDirX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6b41f-121">To get a reference to the PageLineJumpDirX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6b41f-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6b41f-122">Section index:</span></span>  <br/> |<span data-ttu-id="6b41f-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6b41f-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6b41f-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6b41f-124">Row index:</span></span>  <br/> |<span data-ttu-id="6b41f-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="6b41f-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="6b41f-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6b41f-126">Cell index:</span></span>  <br/> |<span data-ttu-id="6b41f-127">**visPLOJumpDirX**</span><span class="sxs-lookup"><span data-stu-id="6b41f-127">**visPLOJumpDirX**</span></span> <br/> |
   

