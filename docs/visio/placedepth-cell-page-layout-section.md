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
# <a name="placedepth-cell-page-layout-section"></a><span data-ttu-id="1aafb-103">Zelle "PlaceDepth" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="1aafb-103">PlaceDepth Cell (Page Layout Section)</span></span>

<span data-ttu-id="1aafb-104">Legt die Methode fest, anhand derer die Zeichnung vor Erstellen des Layouts analysiert wird, und definiert den Layouttyp.</span><span class="sxs-lookup"><span data-stu-id="1aafb-104">Determines the method by which the drawing is analyzed before creating the layout, and determines the type of layout.</span></span>
  
|<span data-ttu-id="1aafb-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="1aafb-105">**Value**</span></span>|<span data-ttu-id="1aafb-106">**Platzierungstiefe für vertikale und horizontale Layouts**</span><span class="sxs-lookup"><span data-stu-id="1aafb-106">**Placement depth for vertical and horizontal layouts**</span></span>|<span data-ttu-id="1aafb-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="1aafb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="1aafb-108">0</span><span class="sxs-lookup"><span data-stu-id="1aafb-108">0</span></span>  <br/> | <span data-ttu-id="1aafb-109">Zeichenblattstandard</span><span class="sxs-lookup"><span data-stu-id="1aafb-109">Page default</span></span>  <br/> |<span data-ttu-id="1aafb-110">**visPLOPlaceDepthDefault**</span><span class="sxs-lookup"><span data-stu-id="1aafb-110">**visPLOPlaceDepthDefault**</span></span> <br/> |
| <span data-ttu-id="1aafb-111">1</span><span class="sxs-lookup"><span data-stu-id="1aafb-111">1</span></span>  <br/> | <span data-ttu-id="1aafb-112">Mittel</span><span class="sxs-lookup"><span data-stu-id="1aafb-112">Medium</span></span>  <br/> |<span data-ttu-id="1aafb-113">**visPLOPlaceDepthMedium**</span><span class="sxs-lookup"><span data-stu-id="1aafb-113">**visPLOPlaceDepthMedium**</span></span> <br/> |
| <span data-ttu-id="1aafb-114">2</span><span class="sxs-lookup"><span data-stu-id="1aafb-114">2</span></span>  <br/> | <span data-ttu-id="1aafb-115">Tiefe</span><span class="sxs-lookup"><span data-stu-id="1aafb-115">Deep</span></span>  <br/> |<span data-ttu-id="1aafb-116">**visPLOPlaceDepthDeep**</span><span class="sxs-lookup"><span data-stu-id="1aafb-116">**visPLOPlaceDepthDeep**</span></span> <br/> |
| <span data-ttu-id="1aafb-117">3</span><span class="sxs-lookup"><span data-stu-id="1aafb-117">3</span></span>  <br/> | <span data-ttu-id="1aafb-118">Flache</span><span class="sxs-lookup"><span data-stu-id="1aafb-118">Shallow</span></span>  <br/> |<span data-ttu-id="1aafb-119">**visPLOPlaceDepthShallow**</span><span class="sxs-lookup"><span data-stu-id="1aafb-119">**visPLOPlaceDepthShallow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1aafb-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1aafb-120">Remarks</span></span>

<span data-ttu-id="1aafb-121">Wenn Sie einen Verweis auf die Zelle Zelle PlaceDepth aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1aafb-121">To get a reference to the PlaceDepth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1aafb-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1aafb-122">Cell name:</span></span>  <br/> | <span data-ttu-id="1aafb-123">Zelle PlaceDepth</span><span class="sxs-lookup"><span data-stu-id="1aafb-123">PlaceDepth</span></span>  <br/> |
   
<span data-ttu-id="1aafb-124">Wenn Sie einen Verweis auf die Zelle Zelle PlaceDepth aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1aafb-124">To get a reference to the PlaceDepth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1aafb-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1aafb-125">Section index:</span></span>  <br/> |<span data-ttu-id="1aafb-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1aafb-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1aafb-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1aafb-127">Row index:</span></span>  <br/> |<span data-ttu-id="1aafb-128">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="1aafb-128">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="1aafb-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1aafb-129">Cell index:</span></span>  <br/> |<span data-ttu-id="1aafb-130">**visPLOPlaceDepth**</span><span class="sxs-lookup"><span data-stu-id="1aafb-130">**visPLOPlaceDepth**</span></span> <br/> |
   

