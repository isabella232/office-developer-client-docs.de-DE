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
ms.openlocfilehash: 21ad1d95fd83780f31778dbc8bb70f9bdb4b922d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414676"
---
# <a name="pagelinejumpdiry-cell-page-layout-section"></a><span data-ttu-id="2fdbc-103">Zelle "PageLineJumpDirY" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="2fdbc-103">PageLineJumpDirY Cell (Page Layout Section)</span></span>

<span data-ttu-id="2fdbc-104">Bestimmt die Richtung von Liniensprüngen auf vertikalen dynamischen Verbindern auf dem Zeichenblatt, für die Sie keine lokale Liniensprungrichtung festgelegt haben.</span><span class="sxs-lookup"><span data-stu-id="2fdbc-104">Determines the direction of line jumps on vertical dynamic connectors on the drawing page for which you haven't applied a local jump direction.</span></span>
  
|<span data-ttu-id="2fdbc-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2fdbc-105">**Value**</span></span>|<span data-ttu-id="2fdbc-106">**Liniensprungrichtung**</span><span class="sxs-lookup"><span data-stu-id="2fdbc-106">**Line jump direction**</span></span>|<span data-ttu-id="2fdbc-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="2fdbc-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2fdbc-108">0</span><span class="sxs-lookup"><span data-stu-id="2fdbc-108">0</span></span>  <br/> | <span data-ttu-id="2fdbc-109">Standard, nach oben oder die Einstellung des Zeichenblatts für Shapes</span><span class="sxs-lookup"><span data-stu-id="2fdbc-109">Default; up or the page's setting for shapes</span></span>  <br/> |<span data-ttu-id="2fdbc-110">**visLOJumpDirYDefault**</span><span class="sxs-lookup"><span data-stu-id="2fdbc-110">**visLOJumpDirYDefault**</span></span> <br/> |
| <span data-ttu-id="2fdbc-111">1</span><span class="sxs-lookup"><span data-stu-id="2fdbc-111">1</span></span>  <br/> | <span data-ttu-id="2fdbc-112">Nach links</span><span class="sxs-lookup"><span data-stu-id="2fdbc-112">Left</span></span>  <br/> |<span data-ttu-id="2fdbc-113">**visLOJumpDirYLeft**</span><span class="sxs-lookup"><span data-stu-id="2fdbc-113">**visLOJumpDirYLeft**</span></span> <br/> |
| <span data-ttu-id="2fdbc-114">2</span><span class="sxs-lookup"><span data-stu-id="2fdbc-114">2</span></span>  <br/> | <span data-ttu-id="2fdbc-115">Nach rechts</span><span class="sxs-lookup"><span data-stu-id="2fdbc-115">Right</span></span>  <br/> |<span data-ttu-id="2fdbc-116">**visLOJumpDirYRight**</span><span class="sxs-lookup"><span data-stu-id="2fdbc-116">**visLOJumpDirYRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fdbc-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fdbc-117">Remarks</span></span>

<span data-ttu-id="2fdbc-118">Wenn Sie einen Verweis auf die Zelle Zelle PageLineJumpDirY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2fdbc-118">To get a reference to the PageLineJumpDirY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2fdbc-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2fdbc-119">Cell name:</span></span>  <br/> | <span data-ttu-id="2fdbc-120">Zelle PageLineJumpDirY</span><span class="sxs-lookup"><span data-stu-id="2fdbc-120">PageLineJumpDirY</span></span>  <br/> |
   
<span data-ttu-id="2fdbc-121">Wenn Sie einen Verweis auf die Zelle Zelle PageLineJumpDirY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2fdbc-121">To get a reference to the PageLineJumpDirY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2fdbc-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2fdbc-122">Section index:</span></span>  <br/> |<span data-ttu-id="2fdbc-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2fdbc-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2fdbc-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2fdbc-124">Row index:</span></span>  <br/> |<span data-ttu-id="2fdbc-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="2fdbc-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="2fdbc-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2fdbc-126">Cell index:</span></span>  <br/> |<span data-ttu-id="2fdbc-127">**visPLOJumpDirY**</span><span class="sxs-lookup"><span data-stu-id="2fdbc-127">**visPLOJumpDirY**</span></span> <br/> |
   

