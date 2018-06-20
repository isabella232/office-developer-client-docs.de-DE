---
title: Zelle "YGridDensity" (Lineal &amp; Rasterabschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251363
localization_priority: Normal
ms.assetid: 3ea2b3c7-0c69-a9f2-379f-8daa0c665810
description: Gibt den Typ des zu verwendenden vertikalen Gitters an.
ms.openlocfilehash: 4e0d1b1dc6f3da95b9328342e0398313b6c85eb4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798470"
---
# <a name="ygriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="97ddb-103">Zelle "YGridDensity" (Lineal &amp; Rasterabschnitt)</span><span class="sxs-lookup"><span data-stu-id="97ddb-103">YGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="97ddb-104">Gibt den Typ des zu verwendenden vertikalen Gitters an.</span><span class="sxs-lookup"><span data-stu-id="97ddb-104">Specifies the type of vertical grid to use.</span></span>
  
|<span data-ttu-id="97ddb-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="97ddb-105">**Value**</span></span>|<span data-ttu-id="97ddb-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97ddb-106">**Description**</span></span>|<span data-ttu-id="97ddb-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="97ddb-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="97ddb-108">0</span><span class="sxs-lookup"><span data-stu-id="97ddb-108">0</span></span>  <br/> |<span data-ttu-id="97ddb-109">Fest</span><span class="sxs-lookup"><span data-stu-id="97ddb-109">Fixed</span></span>  <br/> |<span data-ttu-id="97ddb-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="97ddb-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="97ddb-111">2</span><span class="sxs-lookup"><span data-stu-id="97ddb-111">2</span></span>  <br/> |<span data-ttu-id="97ddb-112">Grob</span><span class="sxs-lookup"><span data-stu-id="97ddb-112">Coarse</span></span>  <br/> |<span data-ttu-id="97ddb-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="97ddb-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="97ddb-114">4</span><span class="sxs-lookup"><span data-stu-id="97ddb-114">4</span></span>  <br/> |<span data-ttu-id="97ddb-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="97ddb-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="97ddb-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="97ddb-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="97ddb-117">8</span><span class="sxs-lookup"><span data-stu-id="97ddb-117">8</span></span>  <br/> |<span data-ttu-id="97ddb-118">Fein</span><span class="sxs-lookup"><span data-stu-id="97ddb-118">Fine</span></span>  <br/> |<span data-ttu-id="97ddb-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="97ddb-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="97ddb-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97ddb-120">Remarks</span></span>

<span data-ttu-id="97ddb-121">Diese Zelle entspricht der vertikalen **Gitterabstand** option in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ).</span><span class="sxs-lookup"><span data-stu-id="97ddb-121">This cell corresponds to the vertical **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="97ddb-122">Wenn Sie einen Verweis auf die Zelle YGridDensity nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="97ddb-122">To get a reference to the YGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97ddb-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="97ddb-123">Cell name:</span></span>  <br/> |<span data-ttu-id="97ddb-124">YGridDensity</span><span class="sxs-lookup"><span data-stu-id="97ddb-124">YGridDensity</span></span>  <br/> |
   
<span data-ttu-id="97ddb-125">Wenn Sie einen Verweis auf die Zelle YGridDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="97ddb-125">To get a reference to the YGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97ddb-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="97ddb-126">Section index:</span></span>  <br/> |<span data-ttu-id="97ddb-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="97ddb-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="97ddb-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="97ddb-128">Row index:</span></span>  <br/> |<span data-ttu-id="97ddb-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="97ddb-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="97ddb-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="97ddb-130">Cell index:</span></span>  <br/> |<span data-ttu-id="97ddb-131">**visYGridDensity**</span><span class="sxs-lookup"><span data-stu-id="97ddb-131">**visYGridDensity**</span></span> <br/> |
   

