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
# <a name="conlinerouteext-cell-shape-layout-section"></a><span data-ttu-id="9edce-103">Zelle "ConLineRouteExt" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="9edce-103">ConLineRouteExt Cell (Shape Layout Section)</span></span>

<span data-ttu-id="9edce-104">Bestimmt die Darstellung eines Verbinders.</span><span class="sxs-lookup"><span data-stu-id="9edce-104">Determines the appearance of a connector.</span></span>
  
|<span data-ttu-id="9edce-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9edce-105">**Value**</span></span>|<span data-ttu-id="9edce-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9edce-106">**Description**</span></span>|<span data-ttu-id="9edce-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="9edce-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9edce-108">0</span><span class="sxs-lookup"><span data-stu-id="9edce-108">0</span></span>  <br/> | <span data-ttu-id="9edce-109">Standard, Zeichenblatteinstellung verwenden</span><span class="sxs-lookup"><span data-stu-id="9edce-109">Default; use page setting</span></span>  <br/> |<span data-ttu-id="9edce-110">**visLORouteExtDefault**</span><span class="sxs-lookup"><span data-stu-id="9edce-110">**visLORouteExtDefault**</span></span> <br/> |
| <span data-ttu-id="9edce-111">1</span><span class="sxs-lookup"><span data-stu-id="9edce-111">1</span></span>  <br/> | <span data-ttu-id="9edce-112">Gerade</span><span class="sxs-lookup"><span data-stu-id="9edce-112">Straight</span></span>  <br/> |<span data-ttu-id="9edce-113">**visLORouteExtStraight**</span><span class="sxs-lookup"><span data-stu-id="9edce-113">**visLORouteExtStraight**</span></span> <br/> |
| <span data-ttu-id="9edce-114">2</span><span class="sxs-lookup"><span data-stu-id="9edce-114">2</span></span>  <br/> | <span data-ttu-id="9edce-115">Gebogene</span><span class="sxs-lookup"><span data-stu-id="9edce-115">Curved</span></span>  <br/> |<span data-ttu-id="9edce-116">**visLORouteExtNURBS**</span><span class="sxs-lookup"><span data-stu-id="9edce-116">**visLORouteExtNURBS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9edce-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9edce-117">Remarks</span></span>

<span data-ttu-id="9edce-118">Wenn Sie einen Verweis auf die Zelle Zelle ConLineRouteExt aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9edce-118">To get a reference to the ConLineRouteExt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9edce-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9edce-119">Cell name:</span></span>  <br/> | <span data-ttu-id="9edce-120">Zelle ConLineRouteExt</span><span class="sxs-lookup"><span data-stu-id="9edce-120">ConLineRouteExt</span></span>  <br/> |
   
<span data-ttu-id="9edce-121">Wenn Sie einen Verweis auf die Zelle Zelle ConLineRouteExt aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9edce-121">To get a reference to the ConLineRouteExt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9edce-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9edce-122">Section index:</span></span>  <br/> |<span data-ttu-id="9edce-123">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9edce-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9edce-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9edce-124">Row index:</span></span>  <br/> |<span data-ttu-id="9edce-125">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="9edce-125">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="9edce-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9edce-126">Cell index:</span></span>  <br/> |<span data-ttu-id="9edce-127">**visSLOLineRouteExt**</span><span class="sxs-lookup"><span data-stu-id="9edce-127">**visSLOLineRouteExt**</span></span> <br/> |
   

