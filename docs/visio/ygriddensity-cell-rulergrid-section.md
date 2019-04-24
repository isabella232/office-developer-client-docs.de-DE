---
title: Zelle YGridDensity Cell (Ruler &amp; Grid section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Gibt den Typ des zu verwendenden vertikalen Gitters an.
ms.openlocfilehash: 793fa40316edd591c8b4873d8919507c2393b5d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307707"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="ad843-103">Zelle YGridDensity Cell (Ruler &amp; Grid section)</span><span class="sxs-lookup"><span data-stu-id="ad843-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="ad843-104">Gibt den Typ des zu verwendenden vertikalen Gitters an.</span><span class="sxs-lookup"><span data-stu-id="ad843-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="ad843-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ad843-105">**Value**</span></span>|<span data-ttu-id="ad843-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ad843-106">**Description**</span></span>|<span data-ttu-id="ad843-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="ad843-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ad843-108">0</span><span class="sxs-lookup"><span data-stu-id="ad843-108">0</span></span>  <br/> |<span data-ttu-id="ad843-109">Fest</span><span class="sxs-lookup"><span data-stu-id="ad843-109">Fixed</span></span>  <br/> |<span data-ttu-id="ad843-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="ad843-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="ad843-111">2</span><span class="sxs-lookup"><span data-stu-id="ad843-111">2</span></span>  <br/> |<span data-ttu-id="ad843-112">Grob</span><span class="sxs-lookup"><span data-stu-id="ad843-112">Coarse</span></span>  <br/> |<span data-ttu-id="ad843-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="ad843-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="ad843-114">4</span><span class="sxs-lookup"><span data-stu-id="ad843-114">4</span></span>  <br/> |<span data-ttu-id="ad843-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="ad843-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="ad843-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="ad843-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="ad843-117">8</span><span class="sxs-lookup"><span data-stu-id="ad843-117">8</span></span>  <br/> |<span data-ttu-id="ad843-118">Abgestimmter</span><span class="sxs-lookup"><span data-stu-id="ad843-118">Fine</span></span>  <br/> |<span data-ttu-id="ad843-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="ad843-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ad843-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ad843-120">Remarks</span></span>

<span data-ttu-id="ad843-121">Diese Zelle entspricht der Option vertikaler **Rasterabstand** im Dialogfeld \*\*\*\* \*\* &amp; Lineal (Raster\*\* ) (Klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil).</span><span class="sxs-lookup"><span data-stu-id="ad843-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="ad843-122">Wenn Sie einen Verweis auf die Zelle Zelle YGridDensity aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ad843-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad843-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ad843-123">Cell name:</span></span>  <br/> |<span data-ttu-id="ad843-124">Zelle YGridDensity</span><span class="sxs-lookup"><span data-stu-id="ad843-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="ad843-125">Wenn Sie einen Verweis auf die Zelle Zelle YGridDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ad843-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ad843-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ad843-126">Section index:</span></span>  <br/> |<span data-ttu-id="ad843-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ad843-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ad843-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ad843-128">Row index:</span></span>  <br/> |<span data-ttu-id="ad843-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="ad843-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="ad843-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ad843-130">Cell index:</span></span>  <br/> |<span data-ttu-id="ad843-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="ad843-131">**visYGridDensity**</span></span> <br/> |
   

