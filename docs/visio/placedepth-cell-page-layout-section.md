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
ms.openlocfilehash: ab2c83a94c3dd03c1fdbf0c3ee187076406b2e84
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797608"
---
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="9e0de-103">PlaceDepth Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="9e0de-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="9e0de-104">Legt die Methode fest, anhand derer die Zeichnung vor Erstellen des Layouts analysiert wird, und definiert den Layouttyp.</span><span class="sxs-lookup"><span data-stu-id="9e0de-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="9e0de-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9e0de-105">**Value**</span></span>|<span data-ttu-id="9e0de-106">**Platzierungstiefe für vertikale und horizontale Layouts**</span><span class="sxs-lookup"><span data-stu-id="9e0de-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="9e0de-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="9e0de-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="9e0de-108">0</span><span class="sxs-lookup"><span data-stu-id="9e0de-108">0</span></span>  <br/> | <span data-ttu-id="9e0de-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="9e0de-109">Page default</span></span>  <br/> |<span data-ttu-id="9e0de-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="9e0de-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="9e0de-111">1</span><span class="sxs-lookup"><span data-stu-id="9e0de-111">1</span></span>  <br/> | <span data-ttu-id="9e0de-112">Mittel</span><span class="sxs-lookup"><span data-stu-id="9e0de-112">Medium</span></span>  <br/> |<span data-ttu-id="9e0de-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="9e0de-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="9e0de-114">2</span><span class="sxs-lookup"><span data-stu-id="9e0de-114">2</span></span>  <br/> | <span data-ttu-id="9e0de-115">Tief</span><span class="sxs-lookup"><span data-stu-id="9e0de-115">Deep</span></span>  <br/> |<span data-ttu-id="9e0de-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="9e0de-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="9e0de-117">3</span><span class="sxs-lookup"><span data-stu-id="9e0de-117">3</span></span>  <br/> | <span data-ttu-id="9e0de-118">Flach</span><span class="sxs-lookup"><span data-stu-id="9e0de-118">Shallow</span></span>  <br/> |<span data-ttu-id="9e0de-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="9e0de-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e0de-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e0de-120">Remarks</span></span>

<span data-ttu-id="9e0de-121">Wenn Sie einen Verweis auf die Zelle PlaceDepth aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9e0de-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e0de-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9e0de-122">Cell name:</span></span>  <br/> | <span data-ttu-id="9e0de-123">PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="9e0de-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="9e0de-124">Wenn Sie einen Verweis auf die Zelle PlaceDepth aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9e0de-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9e0de-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9e0de-125">Section index:</span></span>  <br/> |<span data-ttu-id="9e0de-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9e0de-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9e0de-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9e0de-127">Row index:</span></span>  <br/> |<span data-ttu-id="9e0de-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="9e0de-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="9e0de-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9e0de-129">Cell index:</span></span>  <br/> |<span data-ttu-id="9e0de-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="9e0de-130">**visPLOPlaceDepth**</span></span> <br/> |
   

