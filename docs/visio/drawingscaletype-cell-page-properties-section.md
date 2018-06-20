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
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796908"
---
# <a name="drawingscaletype-cell-page-properties-section"></a><span data-ttu-id="8cf3f-103">DrawingScaleType Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="8cf3f-103">DrawingScaleType Cell (Page Properties Section)</span></span>

<span data-ttu-id="8cf3f-104">Legt den im Dialogfeld **Seite einrichten** ausgewählten Zeichnungsmaßstab fest (klicken Sie auf den Pfeil neben **Seite einrichten** auf der Registerkarte **Start** ).</span><span class="sxs-lookup"><span data-stu-id="8cf3f-104">Determines the drawing scale selected in the **Page Setup** dialog box (click the **Page Setup** arrow on the **Home** tab).</span></span> 
  
|<span data-ttu-id="8cf3f-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-105">**Value**</span></span>|<span data-ttu-id="8cf3f-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-106">**Description**</span></span>|<span data-ttu-id="8cf3f-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="8cf3f-108">0</span><span class="sxs-lookup"><span data-stu-id="8cf3f-108">0</span></span>  <br/> | <span data-ttu-id="8cf3f-109">Kein Maßstab</span><span class="sxs-lookup"><span data-stu-id="8cf3f-109">No Scale</span></span>  <br/> |<span data-ttu-id="8cf3f-110">**visNoScale**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-110">**visNoScale**</span></span> <br/> |
| <span data-ttu-id="8cf3f-111">1</span><span class="sxs-lookup"><span data-stu-id="8cf3f-111">1</span></span>  <br/> | <span data-ttu-id="8cf3f-112">Architekturmaßstab</span><span class="sxs-lookup"><span data-stu-id="8cf3f-112">Architectural Scale</span></span>  <br/> |<span data-ttu-id="8cf3f-113">**visArchitectural**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-113">**visArchitectural**</span></span> <br/> |
| <span data-ttu-id="8cf3f-114">2</span><span class="sxs-lookup"><span data-stu-id="8cf3f-114">2</span></span>  <br/> | <span data-ttu-id="8cf3f-115">Tiefbaumaßstab</span><span class="sxs-lookup"><span data-stu-id="8cf3f-115">Civil Engineering Scale</span></span>  <br/> |<span data-ttu-id="8cf3f-116">**visEngineering**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-116">**visEngineering**</span></span> <br/> |
| <span data-ttu-id="8cf3f-117">3</span><span class="sxs-lookup"><span data-stu-id="8cf3f-117">3</span></span>  <br/> | <span data-ttu-id="8cf3f-118">Benutzerdefinierter Maßstab</span><span class="sxs-lookup"><span data-stu-id="8cf3f-118">Custom Scale</span></span>  <br/> |<span data-ttu-id="8cf3f-119">**visScaleCustom**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-119">**visScaleCustom**</span></span> <br/> |
| <span data-ttu-id="8cf3f-120">4</span><span class="sxs-lookup"><span data-stu-id="8cf3f-120">4</span></span>  <br/> | <span data-ttu-id="8cf3f-121">Metrisch</span><span class="sxs-lookup"><span data-stu-id="8cf3f-121">Metric</span></span>  <br/> |<span data-ttu-id="8cf3f-122">**visScaleMetric**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-122">**visScaleMetric**</span></span> <br/> |
| <span data-ttu-id="8cf3f-123">5</span><span class="sxs-lookup"><span data-stu-id="8cf3f-123">5</span></span>  <br/> | <span data-ttu-id="8cf3f-124">Maschinenbaumaßstab</span><span class="sxs-lookup"><span data-stu-id="8cf3f-124">Mechanical Engineering Scale</span></span>  <br/> |<span data-ttu-id="8cf3f-125">**visScaleMechanical**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-125">**visScaleMechanical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cf3f-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8cf3f-126">Remarks</span></span>

<span data-ttu-id="8cf3f-127">Wenn Sie einen Verweis auf die Zelle DrawingScaleType nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8cf3f-127">To get a reference to the DrawingScaleType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8cf3f-128">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="8cf3f-128">Cell name:</span></span>  <br/> | <span data-ttu-id="8cf3f-129">DrawingScaleType</span><span class="sxs-lookup"><span data-stu-id="8cf3f-129">DrawingScaleType</span></span>  <br/> |
   
<span data-ttu-id="8cf3f-130">Wenn Sie einen Verweis auf die Zelle DrawingScaleType aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="8cf3f-130">To get a reference to the DrawingScaleType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8cf3f-131">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="8cf3f-131">Section index:</span></span>  <br/> |<span data-ttu-id="8cf3f-132">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-132">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8cf3f-133">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="8cf3f-133">Row index:</span></span>  <br/> |<span data-ttu-id="8cf3f-134">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-134">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="8cf3f-135">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="8cf3f-135">Cell index:</span></span>  <br/> |<span data-ttu-id="8cf3f-136">**visPageDrawScaleType**</span><span class="sxs-lookup"><span data-stu-id="8cf3f-136">**visPageDrawScaleType**</span></span> <br/> |
   

