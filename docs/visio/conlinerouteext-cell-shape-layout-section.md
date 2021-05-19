---
title: Zelle "ConLineRouteExt" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50110
localization_priority: Normal
ms.assetid: cafd7589-1c94-b9bc-b1a6-40f7c15fba71
description: Bestimmt die Darstellung eines Verbinders.
ms.openlocfilehash: 19fe948daf7aa3d67db858849ecb2b15f40ba02d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434613"
---
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="58679-103">Zelle "ConLineRouteExt" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="58679-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="58679-104">Bestimmt die Darstellung eines Verbinders.</span><span class="sxs-lookup"><span data-stu-id="58679-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="58679-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="58679-105">**Value**</span></span>|<span data-ttu-id="58679-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="58679-106">**Description**</span></span>|<span data-ttu-id="58679-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="58679-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="58679-108">0</span><span class="sxs-lookup"><span data-stu-id="58679-108">0</span></span>  <br/> | <span data-ttu-id="58679-109">Standard, Zeichenblatteinstellung verwenden</span><span class="sxs-lookup"><span data-stu-id="58679-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="58679-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="58679-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="58679-111">1</span><span class="sxs-lookup"><span data-stu-id="58679-111">1</span></span>  <br/> | <span data-ttu-id="58679-112">Straight</span><span class="sxs-lookup"><span data-stu-id="58679-112">Straight</span></span>  <br/> |<span data-ttu-id="58679-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="58679-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="58679-114">2</span><span class="sxs-lookup"><span data-stu-id="58679-114">2</span></span>  <br/> | <span data-ttu-id="58679-115">Gekrümmt</span><span class="sxs-lookup"><span data-stu-id="58679-115">Curved</span></span>  <br/> |<span data-ttu-id="58679-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="58679-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58679-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="58679-117">Remarks</span></span>

<span data-ttu-id="58679-118">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ConLineRouteExt anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="58679-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58679-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="58679-119">Cell name:</span></span>  <br/> | <span data-ttu-id="58679-120">ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="58679-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="58679-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ConLineRouteExt-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="58679-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58679-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="58679-122">Section index:</span></span>  <br/> |<span data-ttu-id="58679-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="58679-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="58679-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="58679-124">Row index:</span></span>  <br/> |<span data-ttu-id="58679-125">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="58679-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="58679-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="58679-126">Cell index:</span></span>  <br/> |<span data-ttu-id="58679-127">**visSLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="58679-127">**visSLOLineRouteExt**</span></span> <br/> |
   

