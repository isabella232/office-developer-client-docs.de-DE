---
title: Zelle "DrawingScaleType" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: Legt den im Dialogfeld Seite einrichten ausgewählten Zeichnungsmaßstab fest (klicken Sie auf der Registerkarte Start auf den Pfeil neben Seite einrichten).
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428739"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="49401-103">Zelle "DrawingScaleType" (Abschnitt "Page Properties")</span><span class="sxs-lookup"><span data-stu-id="49401-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="49401-104">Legt den im Dialogfeld **Seite einrichten** ausgewählten Zeichnungsmaßstab fest (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Seite einrichten**).</span><span class="sxs-lookup"><span data-stu-id="49401-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="49401-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="49401-105">**Value**</span></span>|<span data-ttu-id="49401-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="49401-106">**Description**</span></span>|<span data-ttu-id="49401-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="49401-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="49401-108">0</span><span class="sxs-lookup"><span data-stu-id="49401-108">0</span></span>  <br/> | <span data-ttu-id="49401-109">Kein Maßstab</span><span class="sxs-lookup"><span data-stu-id="49401-109">No Scale</span></span>  <br/> |<span data-ttu-id="49401-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="49401-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="49401-111">1</span><span class="sxs-lookup"><span data-stu-id="49401-111">1</span></span>  <br/> | <span data-ttu-id="49401-112">Architekturmaßstab</span><span class="sxs-lookup"><span data-stu-id="49401-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="49401-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="49401-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="49401-114">2</span><span class="sxs-lookup"><span data-stu-id="49401-114">2</span></span>  <br/> | <span data-ttu-id="49401-115">Tiefbaumaßstab</span><span class="sxs-lookup"><span data-stu-id="49401-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="49401-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="49401-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="49401-117">3</span><span class="sxs-lookup"><span data-stu-id="49401-117">3</span></span>  <br/> | <span data-ttu-id="49401-118">Benutzerdefinierter Maßstab</span><span class="sxs-lookup"><span data-stu-id="49401-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="49401-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="49401-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="49401-120">4 </span><span class="sxs-lookup"><span data-stu-id="49401-120">4</span></span>  <br/> | <span data-ttu-id="49401-121">Metrik</span><span class="sxs-lookup"><span data-stu-id="49401-121">Metric</span></span>  <br/> |<span data-ttu-id="49401-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="49401-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="49401-123">5 </span><span class="sxs-lookup"><span data-stu-id="49401-123">5</span></span>  <br/> | <span data-ttu-id="49401-124">Maschinenbaumaßstab</span><span class="sxs-lookup"><span data-stu-id="49401-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="49401-125">**visScaleChanal**</span><span class="sxs-lookup"><span data-stu-id="49401-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="49401-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="49401-126">Remarks</span></span>

<span data-ttu-id="49401-127">Um einen Verweis auf die Zelle DrawingScaleType anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="49401-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="49401-128">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="49401-128">Cell name:</span></span>  <br/> | <span data-ttu-id="49401-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="49401-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="49401-130">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DrawingScaleType-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="49401-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="49401-131">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="49401-131">Section index:</span></span>  <br/> |<span data-ttu-id="49401-132">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="49401-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="49401-133">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="49401-133">Row index:</span></span>  <br/> |<span data-ttu-id="49401-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="49401-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="49401-135">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="49401-135">Cell index:</span></span>  <br/> |<span data-ttu-id="49401-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="49401-136">**visPageDrawScaleType**</span></span> <br/> |
   

