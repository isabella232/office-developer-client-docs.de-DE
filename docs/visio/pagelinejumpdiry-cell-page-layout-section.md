---
title: Zelle "PageLineJumpDirY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm770
localization_priority: Normal
ms.assetid: f73cc157-b332-279b-f7cf-d5a090bc09a4
description: Bestimmt die Richtung von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.
ms.openlocfilehash: 640ad93fbccf2cec26bda535c288c881aea32207
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797595"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="db76e-103">PageLineJumpDirY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="db76e-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="db76e-104">Bestimmt die Richtung von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="db76e-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="db76e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="db76e-105">**Value**</span></span>|<span data-ttu-id="db76e-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="db76e-106">**Line jump direction**</span></span>|<span data-ttu-id="db76e-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="db76e-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="db76e-108">0</span><span class="sxs-lookup"><span data-stu-id="db76e-108">0</span></span>  <br/> | <span data-ttu-id="db76e-109">Standard, nach oben oder die Einstellung des Zeichenblatts für Shapes</span><span class="sxs-lookup"><span data-stu-id="db76e-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="db76e-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="db76e-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="db76e-111">1</span><span class="sxs-lookup"><span data-stu-id="db76e-111">1</span></span>  <br/> | <span data-ttu-id="db76e-112">Nach links</span><span class="sxs-lookup"><span data-stu-id="db76e-112">Left</span></span>  <br/> |<span data-ttu-id="db76e-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="db76e-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="db76e-114">2</span><span class="sxs-lookup"><span data-stu-id="db76e-114">2</span></span>  <br/> | <span data-ttu-id="db76e-115">Nach rechts</span><span class="sxs-lookup"><span data-stu-id="db76e-115">Right</span></span>  <br/> |<span data-ttu-id="db76e-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="db76e-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db76e-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db76e-117">Remarks</span></span>

<span data-ttu-id="db76e-118">Wenn Sie einen Verweis auf die Zelle PageLineJumpDirY aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="db76e-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db76e-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="db76e-119">Cell name:</span></span>  <br/> | <span data-ttu-id="db76e-120">PageLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="db76e-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="db76e-121">Wenn Sie einen Verweis auf die Zelle PageLineJumpDirY aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="db76e-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="db76e-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="db76e-122">Section index:</span></span>  <br/> |<span data-ttu-id="db76e-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="db76e-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="db76e-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="db76e-124">Row index:</span></span>  <br/> |<span data-ttu-id="db76e-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="db76e-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="db76e-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="db76e-126">Cell index:</span></span>  <br/> |<span data-ttu-id="db76e-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="db76e-127">**visPLOJumpDirY**</span></span> <br/> |
   

