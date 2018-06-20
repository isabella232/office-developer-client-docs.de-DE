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
ms.openlocfilehash: 21da283f2d9ab43837b8fe4127840e89ea9d9949
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797347"
---
# <a name="linerouteext-cell-page-layout-section"></a><span data-ttu-id="aae71-103">LineRouteExt Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="aae71-103">LineRouteExt Cell (Page Layout Section)</span></span>

<span data-ttu-id="aae71-104">Legt das standardmäßige Erscheinungsbild für sämtliche Verbinder auf einem Zeichenblatt fest.</span><span class="sxs-lookup"><span data-stu-id="aae71-104">Determines the default appearance for all connectors on a drawing page.</span></span>
  
|<span data-ttu-id="aae71-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="aae71-105">**Value**</span></span>|<span data-ttu-id="aae71-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aae71-106">**Description**</span></span>|<span data-ttu-id="aae71-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="aae71-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="aae71-108">0</span><span class="sxs-lookup"><span data-stu-id="aae71-108">0</span></span>  <br/> | <span data-ttu-id="aae71-109">Standardeinstellung (gerade)</span><span class="sxs-lookup"><span data-stu-id="aae71-109">Default (straight)</span></span>  <br/> |<span data-ttu-id="aae71-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="aae71-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="aae71-111">1</span><span class="sxs-lookup"><span data-stu-id="aae71-111">1</span></span>  <br/> | <span data-ttu-id="aae71-112">Gerade</span><span class="sxs-lookup"><span data-stu-id="aae71-112">Straight</span></span>  <br/> |<span data-ttu-id="aae71-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="aae71-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="aae71-114">2</span><span class="sxs-lookup"><span data-stu-id="aae71-114">2</span></span>  <br/> | <span data-ttu-id="aae71-115">Gekrümmt</span><span class="sxs-lookup"><span data-stu-id="aae71-115">Curved</span></span>  <br/> |<span data-ttu-id="aae71-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="aae71-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aae71-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="aae71-117">Remarks</span></span>

<span data-ttu-id="aae71-118">Wenn Sie einen Verweis auf die Zelle LineRouteExt nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="aae71-118">To get a reference to the LineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aae71-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="aae71-119">Cell name:</span></span>  <br/> | <span data-ttu-id="aae71-120">LineRouteExt</span><span class="sxs-lookup"><span data-stu-id="aae71-120">LineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="aae71-121">Wenn Sie einen Verweis auf die Zelle LineRouteExt aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="aae71-121">To get a reference to the LineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="aae71-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="aae71-122">Section index:</span></span>  <br/> |<span data-ttu-id="aae71-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="aae71-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="aae71-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="aae71-124">Row index:</span></span>  <br/> |<span data-ttu-id="aae71-125">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="aae71-125">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="aae71-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="aae71-126">Cell index:</span></span>  <br/> |<span data-ttu-id="aae71-127">**visPLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="aae71-127">**visPLOLineRouteExt**</span></span> <br/> |
   

