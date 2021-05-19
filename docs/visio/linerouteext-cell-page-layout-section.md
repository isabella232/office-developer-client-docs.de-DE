---
title: Zelle "LineRouteExt" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50115
localization_priority: Normal
ms.assetid: 3d16b8b3-601b-c10b-68a8-ffd47251306f
description: Legt das standardmäßige Erscheinungsbild für sämtliche Verbinder auf einem Zeichenblatt fest.
ms.openlocfilehash: 6daed2e06f7673e5a4ec97ec83dc31bad2766301
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410623"
---
# <a name="linerouteext-cell-page-layout-section"></a><span data-ttu-id="c90cb-103">Zelle "LineRouteExt" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="c90cb-103">LineRouteExt Cell (Page Layout Section)</span></span>

<span data-ttu-id="c90cb-104">Legt das standardmäßige Erscheinungsbild für sämtliche Verbinder auf einem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="c90cb-104">Determines the default appearance for all connectors on a drawing page.</span></span>
  
|<span data-ttu-id="c90cb-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c90cb-105">**Value**</span></span>|<span data-ttu-id="c90cb-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c90cb-106">**Description**</span></span>|<span data-ttu-id="c90cb-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="c90cb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c90cb-108">0</span><span class="sxs-lookup"><span data-stu-id="c90cb-108">0</span></span>  <br/> | <span data-ttu-id="c90cb-109">Standardeinstellung (gerade)</span><span class="sxs-lookup"><span data-stu-id="c90cb-109">Default (straight)</span></span>  <br/> |<span data-ttu-id="c90cb-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="c90cb-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="c90cb-111">1</span><span class="sxs-lookup"><span data-stu-id="c90cb-111">1</span></span>  <br/> | <span data-ttu-id="c90cb-112">Straight</span><span class="sxs-lookup"><span data-stu-id="c90cb-112">Straight</span></span>  <br/> |<span data-ttu-id="c90cb-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="c90cb-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="c90cb-114">2</span><span class="sxs-lookup"><span data-stu-id="c90cb-114">2</span></span>  <br/> | <span data-ttu-id="c90cb-115">Gekrümmt</span><span class="sxs-lookup"><span data-stu-id="c90cb-115">Curved</span></span>  <br/> |<span data-ttu-id="c90cb-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="c90cb-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c90cb-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c90cb-117">Remarks</span></span>

<span data-ttu-id="c90cb-118">Verwenden Sie zum Erhalten eines Verweises auf die Zelle LineRouteExt anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="c90cb-118">To get a reference to the LineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c90cb-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c90cb-119">Cell name:</span></span>  <br/> | <span data-ttu-id="c90cb-120">LineRouteExt</span><span class="sxs-lookup"><span data-stu-id="c90cb-120">LineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="c90cb-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LineRouteExt-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c90cb-121">To get a reference to the LineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c90cb-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c90cb-122">Section index:</span></span>  <br/> |<span data-ttu-id="c90cb-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c90cb-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c90cb-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c90cb-124">Row index:</span></span>  <br/> |<span data-ttu-id="c90cb-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="c90cb-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="c90cb-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c90cb-126">Cell index:</span></span>  <br/> |<span data-ttu-id="c90cb-127">**visPLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="c90cb-127">**visPLOLineRouteExt**</span></span> <br/> |
   

