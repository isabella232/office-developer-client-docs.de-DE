---
title: XGridDensity Cell (Ruler &amp; Grid Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1150
localization_priority: Normal
ms.assetid: db7b353f-4379-8865-1c35-36b89cf93257
description: Gibt den Typ des zu verwendenden horizontalen Gitters an.
ms.openlocfilehash: 107cde8e8b0d630a4dc4b43127412de2f6b0115d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798440"
---
# <a name="xgriddensity-cell-ruler-amp-grid-section"></a><span data-ttu-id="86524-103">XGridDensity Cell (Ruler &amp; Grid Section)</span><span class="sxs-lookup"><span data-stu-id="86524-103">XGridDensity Cell (Ruler &amp; Grid Section)</span></span>

<span data-ttu-id="86524-104">Gibt den Typ des zu verwendenden horizontalen Gitters an.</span><span class="sxs-lookup"><span data-stu-id="86524-104">Specifies the type of horizontal grid to use.</span></span>
  
|<span data-ttu-id="86524-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="86524-105">**Value**</span></span>|<span data-ttu-id="86524-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86524-106">**Description**</span></span>|<span data-ttu-id="86524-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="86524-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="86524-108">0</span><span class="sxs-lookup"><span data-stu-id="86524-108">0</span></span>  <br/> |<span data-ttu-id="86524-109">Fest</span><span class="sxs-lookup"><span data-stu-id="86524-109">Fixed</span></span>  <br/> |<span data-ttu-id="86524-110">**visGridFixed**</span><span class="sxs-lookup"><span data-stu-id="86524-110">**visGridFixed**</span></span> <br/> |
|<span data-ttu-id="86524-111">2</span><span class="sxs-lookup"><span data-stu-id="86524-111">2</span></span>  <br/> |<span data-ttu-id="86524-112">Grob</span><span class="sxs-lookup"><span data-stu-id="86524-112">Coarse</span></span>  <br/> |<span data-ttu-id="86524-113">**visGridCoarse**</span><span class="sxs-lookup"><span data-stu-id="86524-113">**visGridCoarse**</span></span> <br/> |
|<span data-ttu-id="86524-114">4</span><span class="sxs-lookup"><span data-stu-id="86524-114">4</span></span>  <br/> |<span data-ttu-id="86524-115">Normal (Standard)</span><span class="sxs-lookup"><span data-stu-id="86524-115">Normal (default)</span></span>  <br/> |<span data-ttu-id="86524-116">**visGridNormal**</span><span class="sxs-lookup"><span data-stu-id="86524-116">**visGridNormal**</span></span> <br/> |
|<span data-ttu-id="86524-117">8</span><span class="sxs-lookup"><span data-stu-id="86524-117">8</span></span>  <br/> |<span data-ttu-id="86524-118">Fein</span><span class="sxs-lookup"><span data-stu-id="86524-118">Fine</span></span>  <br/> |<span data-ttu-id="86524-119">**visGridFine**</span><span class="sxs-lookup"><span data-stu-id="86524-119">**visGridFine**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86524-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="86524-120">Remarks</span></span>

<span data-ttu-id="86524-121">Diese Zelle entspricht der horizontalen **Gitterabstand** option in der **Lineal &amp; Raster** im Dialogfeld (klicken Sie auf der Registerkarte **Ansicht** auf den Pfeil neben **Anzeigen** ).</span><span class="sxs-lookup"><span data-stu-id="86524-121">This cell corresponds to the horizontal **Grid spacing** option in the **Ruler &amp; Grid** dialog box (on the **View** tab, click the **Show** arrow).</span></span> 
  
<span data-ttu-id="86524-122">Wenn Sie einen Verweis auf die Zelle XGridDensity aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="86524-122">To get a reference to the XGridDensity cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86524-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="86524-123">Cell name:</span></span>  <br/> |<span data-ttu-id="86524-124">XGridDensity</span><span class="sxs-lookup"><span data-stu-id="86524-124">XGridDensity</span></span>  <br/> |
   
<span data-ttu-id="86524-125">Wenn Sie einen Verweis auf die Zelle XGridDensity aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="86524-125">To get a reference to the XGridDensity cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86524-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="86524-126">Section index:</span></span>  <br/> |<span data-ttu-id="86524-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="86524-127">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="86524-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="86524-128">Row index:</span></span>  <br/> |<span data-ttu-id="86524-129">**visRowRulerGrid**</span><span class="sxs-lookup"><span data-stu-id="86524-129">**visRowRulerGrid**</span></span> <br/> |
|<span data-ttu-id="86524-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="86524-130">Cell index:</span></span>  <br/> |<span data-ttu-id="86524-131">**visXGridDensity**</span><span class="sxs-lookup"><span data-stu-id="86524-131">**visXGridDensity**</span></span> <br/> |
   

