---
title: XRulerDensity Cell (Ruler &amp; Grid Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1165
localization_priority: Normal
ms.assetid: c11717c5-eb0e-e4fa-5a91-c62ecc048635
description: Legt die horizontalen Einteilungen auf dem Lineal des Zeichenblatts fest.
ms.openlocfilehash: 633b2e54ca77216fd20ead00f047283c54f8164d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798436"
---
# <a name="xrulerdensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="a9a1d-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span><span class="sxs-lookup"><span data-stu-id="a9a1d-103">XRulerDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="a9a1d-104">Legt die horizontalen Einteilungen auf dem Lineal des Zeichenblatts fest.</span><span class="sxs-lookup"><span data-stu-id="a9a1d-104">Specifies the horizontal subdivisions on the ruler for the page.</span></span>
  
|<span data-ttu-id="a9a1d-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-105">**Value**</span></span>|<span data-ttu-id="a9a1d-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-106">**Description**</span></span>|<span data-ttu-id="a9a1d-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a9a1d-108">0</span><span class="sxs-lookup"><span data-stu-id="a9a1d-108">0</span></span>  <br/> |<span data-ttu-id="a9a1d-109">Fest</span><span class="sxs-lookup"><span data-stu-id="a9a1d-109">Fixed</span></span>  <br/> |<span data-ttu-id="a9a1d-110">**visRulerFixed**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-110">**visRulerFixed**</span></span> <br/> |
|<span data-ttu-id="a9a1d-111">8 (&amp;H8)</span><span class="sxs-lookup"><span data-stu-id="a9a1d-111">8 (&amp;H8)</span></span>  <br/> |<span data-ttu-id="a9a1d-112">Grob</span><span class="sxs-lookup"><span data-stu-id="a9a1d-112">Coarse</span></span>  <br/> |<span data-ttu-id="a9a1d-113">**visRulerCoarse**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-113">**visRulerCoarse**</span></span> <br/> |
|<span data-ttu-id="a9a1d-114">16 (&amp;H10)</span><span class="sxs-lookup"><span data-stu-id="a9a1d-114">16 (&amp;H10)</span></span>  <br/> |<span data-ttu-id="a9a1d-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="a9a1d-115">Normal (Default)</span></span>  <br/> |<span data-ttu-id="a9a1d-116">**visRulerNormal**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-116">**visRulerNormal**</span></span> <br/> |
|<span data-ttu-id="a9a1d-117">32 (&amp;H20)</span><span class="sxs-lookup"><span data-stu-id="a9a1d-117">32 (&amp;H20)</span></span>  <br/> |<span data-ttu-id="a9a1d-118">Fein</span><span class="sxs-lookup"><span data-stu-id="a9a1d-118">Fine</span></span>  <br/> |<span data-ttu-id="a9a1d-119">**visRulerFine**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-119">**visRulerFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9a1d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9a1d-120">Remarks</span></span>

<span data-ttu-id="a9a1d-121">Diese Zelle entspricht der horizontalen Option **Einteilung** in die **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ).</span><span class="sxs-lookup"><span data-stu-id="a9a1d-121">This cell corresponds to the horizontal **Subdivisions** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="a9a1d-122">Wenn Sie einen Verweis auf die Zelle XRulerDensity aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a9a1d-122">To get a reference to the XRulerDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9a1d-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a9a1d-123">Cell name:</span></span>  <br/> |<span data-ttu-id="a9a1d-124">XRulerDensity</span><span class="sxs-lookup"><span data-stu-id="a9a1d-124">XRulerDensity</span></span>  <br/> |
   
<span data-ttu-id="a9a1d-125">Wenn Sie einen Verweis auf die Zelle XRulerDensity aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a9a1d-125">To get a reference to the XRulerDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a9a1d-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a9a1d-126">Section index:</span></span>  <br/> |<span data-ttu-id="a9a1d-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a9a1d-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a9a1d-128">Row index:</span></span>  <br/> |<span data-ttu-id="a9a1d-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="a9a1d-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a9a1d-130">Cell index:</span></span>  <br/> |<span data-ttu-id="a9a1d-131">**visXRulerDensity**</span><span class="sxs-lookup"><span data-stu-id="a9a1d-131">**visXRulerDensity**</span></span> <br/> |
   

