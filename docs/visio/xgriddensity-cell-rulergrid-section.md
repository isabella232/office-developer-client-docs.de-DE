---
title: Zelle XGridDensity Cell (Ruler &amp; Grid section)
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328987"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="24598-103">Zelle XGridDensity Cell (Ruler &amp; Grid section)</span><span class="sxs-lookup"><span data-stu-id="24598-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="24598-104">Gibt den Typ des zu verwendenden horizontalen Gitters an.</span><span class="sxs-lookup"><span data-stu-id="24598-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="24598-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="24598-105">**Value**</span></span>|<span data-ttu-id="24598-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24598-106">**Description**</span></span>|<span data-ttu-id="24598-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="24598-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="24598-108">0</span><span class="sxs-lookup"><span data-stu-id="24598-108">0</span></span>  <br/> |<span data-ttu-id="24598-109">Fest</span><span class="sxs-lookup"><span data-stu-id="24598-109">Fixed</span></span>  <br/> |<span data-ttu-id="24598-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="24598-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="24598-111">2</span><span class="sxs-lookup"><span data-stu-id="24598-111">2</span></span>  <br/> |<span data-ttu-id="24598-112">Grob</span><span class="sxs-lookup"><span data-stu-id="24598-112">Coarse</span></span>  <br/> |<span data-ttu-id="24598-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="24598-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="24598-114">4</span><span class="sxs-lookup"><span data-stu-id="24598-114">4</span></span>  <br/> |<span data-ttu-id="24598-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="24598-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="24598-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="24598-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="24598-117">8</span><span class="sxs-lookup"><span data-stu-id="24598-117">8</span></span>  <br/> |<span data-ttu-id="24598-118">Abgestimmter</span><span class="sxs-lookup"><span data-stu-id="24598-118">Fine</span></span>  <br/> |<span data-ttu-id="24598-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="24598-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24598-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="24598-120">Remarks</span></span>

<span data-ttu-id="24598-121">Diese Zelle entspricht der horizontalen **Rasterabstand** Option im Dialogfeld **Lineal &amp; -Raster** (Klicken Sie auf der Registerkarte **Ansicht** auf \*\*\*\* den Pfeil).</span><span class="sxs-lookup"><span data-stu-id="24598-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="24598-122">Wenn Sie einen Verweis auf die Zelle Zelle XGridDensity aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="24598-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24598-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="24598-123">Cell name:</span></span>  <br/> |<span data-ttu-id="24598-124">Zelle XGridDensity</span><span class="sxs-lookup"><span data-stu-id="24598-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="24598-125">Wenn Sie einen Verweis auf die Zelle Zelle XGridDensity aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="24598-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24598-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="24598-126">Section index:</span></span>  <br/> |<span data-ttu-id="24598-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24598-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="24598-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24598-128">Row index:</span></span>  <br/> |<span data-ttu-id="24598-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="24598-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="24598-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="24598-130">Cell index:</span></span>  <br/> |<span data-ttu-id="24598-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="24598-131">**visXGridDensity**</span></span> <br/> |
   

