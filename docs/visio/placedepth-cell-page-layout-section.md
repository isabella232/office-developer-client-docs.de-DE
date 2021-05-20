---
title: Zelle "PlaceDepth" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
localization_priority: Normal
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: Legt die Methode fest, anhand derer die Zeichnung vor Erstellen des Layouts analysiert wird, und definiert den Layouttyp.
ms.openlocfilehash: 463c7dad39955161538aa89d1482685189bf7fdc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432037"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="340ca-103">Zelle "PlaceDepth" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="340ca-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="340ca-104">Legt die Methode fest, anhand derer die Zeichnung vor Erstellen des Layouts analysiert wird, und definiert den Layouttyp.</span><span class="sxs-lookup"><span data-stu-id="340ca-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="340ca-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="340ca-105">**Value**</span></span>|<span data-ttu-id="340ca-106">**Platzierungstiefe für vertikale und horizontale Layouts**</span><span class="sxs-lookup"><span data-stu-id="340ca-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="340ca-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="340ca-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="340ca-108">0</span><span class="sxs-lookup"><span data-stu-id="340ca-108">0</span></span>  <br/> | <span data-ttu-id="340ca-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="340ca-109">Page default</span></span>  <br/> |<span data-ttu-id="340ca-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="340ca-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="340ca-111">1</span><span class="sxs-lookup"><span data-stu-id="340ca-111">1</span></span>  <br/> | <span data-ttu-id="340ca-112">Mittel</span><span class="sxs-lookup"><span data-stu-id="340ca-112">Medium</span></span>  <br/> |<span data-ttu-id="340ca-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="340ca-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="340ca-114">2</span><span class="sxs-lookup"><span data-stu-id="340ca-114">2</span></span>  <br/> | <span data-ttu-id="340ca-115">Deep</span><span class="sxs-lookup"><span data-stu-id="340ca-115">Deep</span></span>  <br/> |<span data-ttu-id="340ca-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="340ca-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="340ca-117">3</span><span class="sxs-lookup"><span data-stu-id="340ca-117">3</span></span>  <br/> | <span data-ttu-id="340ca-118">Flach</span><span class="sxs-lookup"><span data-stu-id="340ca-118">Shallow</span></span>  <br/> |<span data-ttu-id="340ca-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="340ca-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="340ca-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="340ca-120">Remarks</span></span>

<span data-ttu-id="340ca-121">Um einen Verweis auf die Zelle PlaceDepth anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="340ca-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="340ca-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="340ca-122">Cell name:</span></span>  <br/> | <span data-ttu-id="340ca-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="340ca-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="340ca-124">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die PlaceDepth-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="340ca-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="340ca-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="340ca-125">Section index:</span></span>  <br/> |<span data-ttu-id="340ca-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="340ca-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="340ca-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="340ca-127">Row index:</span></span>  <br/> |<span data-ttu-id="340ca-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="340ca-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="340ca-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="340ca-129">Cell index:</span></span>  <br/> |<span data-ttu-id="340ca-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="340ca-130">**visPLOPlaceDepth**</span></span> <br/> |
   

