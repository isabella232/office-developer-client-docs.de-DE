---
title: Zelle "XGridDensity" (Abschnitt "Ruler &amp; Grid")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Gibt den Typ des zu verwendenden horizontalen Gitters an.
ms.openlocfilehash: 5ebd172e56a66bfb39bd9bfa20967bb6b52c5aa2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436041"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="f0d6c-103">Zelle "XGridDensity" (Abschnitt "Ruler &amp; Grid")</span><span class="sxs-lookup"><span data-stu-id="f0d6c-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="f0d6c-104">Gibt den Typ des zu verwendenden horizontalen Gitters an.</span><span class="sxs-lookup"><span data-stu-id="f0d6c-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="f0d6c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-105">**Value**</span></span>|<span data-ttu-id="f0d6c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-106">**Description**</span></span>|<span data-ttu-id="f0d6c-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f0d6c-108">0</span><span class="sxs-lookup"><span data-stu-id="f0d6c-108">0</span></span>  <br/> |<span data-ttu-id="f0d6c-109">Fest</span><span class="sxs-lookup"><span data-stu-id="f0d6c-109">Fixed</span></span>  <br/> |<span data-ttu-id="f0d6c-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="f0d6c-111">2</span><span class="sxs-lookup"><span data-stu-id="f0d6c-111">2</span></span>  <br/> |<span data-ttu-id="f0d6c-112">Vorschrr</span><span class="sxs-lookup"><span data-stu-id="f0d6c-112">Coarse</span></span>  <br/> |<span data-ttu-id="f0d6c-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="f0d6c-114">4 </span><span class="sxs-lookup"><span data-stu-id="f0d6c-114">4</span></span>  <br/> |<span data-ttu-id="f0d6c-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="f0d6c-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="f0d6c-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="f0d6c-117">8 </span><span class="sxs-lookup"><span data-stu-id="f0d6c-117">8</span></span>  <br/> |<span data-ttu-id="f0d6c-118">Fine</span><span class="sxs-lookup"><span data-stu-id="f0d6c-118">Fine</span></span>  <br/> |<span data-ttu-id="f0d6c-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0d6c-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f0d6c-120">Remarks</span></span>

<span data-ttu-id="f0d6c-121">Diese Zelle entspricht der **Horizontalrasterabstandsoption** im Dialogfeld  **&amp; Linealraster** (klicken Sie auf der Registerkarte Ansicht auf den **Pfeil anzeigen).**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="f0d6c-122">Um einen Verweis auf die Zelle XGridDensity anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="f0d6c-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0d6c-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f0d6c-123">Cell name:</span></span>  <br/> |<span data-ttu-id="f0d6c-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="f0d6c-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="f0d6c-125">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die XGridDensity-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="f0d6c-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0d6c-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f0d6c-126">Section index:</span></span>  <br/> |<span data-ttu-id="f0d6c-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f0d6c-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f0d6c-128">Row index:</span></span>  <br/> |<span data-ttu-id="f0d6c-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="f0d6c-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f0d6c-130">Cell index:</span></span>  <br/> |<span data-ttu-id="f0d6c-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="f0d6c-131">**visXGridDensity**</span></span> <br/> |
   

