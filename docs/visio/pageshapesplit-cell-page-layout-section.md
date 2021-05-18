---
title: Zelle "PageShapeSplit" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422019"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="b4be5-103">Zelle "PageShapeSplit" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="b4be5-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="b4be5-104">Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.</span><span class="sxs-lookup"><span data-stu-id="b4be5-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="b4be5-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b4be5-105">**Value**</span></span>|<span data-ttu-id="b4be5-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b4be5-106">**Description**</span></span>|<span data-ttu-id="b4be5-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="b4be5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b4be5-108">0</span><span class="sxs-lookup"><span data-stu-id="b4be5-108">0</span></span>  <br/> |<span data-ttu-id="b4be5-109">Automatische Shape-Teilung nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="b4be5-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="b4be5-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="b4be5-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="b4be5-111">1</span><span class="sxs-lookup"><span data-stu-id="b4be5-111">1</span></span>  <br/> |<span data-ttu-id="b4be5-112">Automatische Shape-Teilung zulassen (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="b4be5-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="b4be5-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="b4be5-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b4be5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b4be5-114">Remarks</span></span>

<span data-ttu-id="b4be5-p101">Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. Die Standardeinstellungen für Shapes hängen vom Typ der Zeichnung ab.</span><span class="sxs-lookup"><span data-stu-id="b4be5-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page levels. The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="b4be5-118">Verwenden Sie zum Aktivieren oder Deaktivieren der  Aufteilung auf Anwendungsebene  die Einstellung Connectorteilung aktivieren auf der Registerkarte Erweitert im Dialogfeld  **Visio-Optionen** (klicken Sie auf die Schaltfläche **Office,** klicken Sie auf der Registerkarte **Visio** auf Optionen, und klicken Sie dann auf **Erweitert** ).</span><span class="sxs-lookup"><span data-stu-id="b4be5-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="b4be5-119">Informationen zum Aktivieren oder Deaktivieren der Aufteilung auf Formebene finden Sie in den Zellen ShapeSplit und ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="b4be5-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="b4be5-120">Um einen Verweis auf die Zelle PageShapeSplit anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="b4be5-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4be5-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b4be5-121">Cell name:</span></span>  <br/> |<span data-ttu-id="b4be5-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="b4be5-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="b4be5-123">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PageShapeSplit nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b4be5-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b4be5-124">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b4be5-124">Section index:</span></span>  <br/> |<span data-ttu-id="b4be5-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b4be5-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b4be5-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b4be5-126">Row index:</span></span>  <br/> |<span data-ttu-id="b4be5-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b4be5-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b4be5-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b4be5-128">Cell index:</span></span>  <br/> |<span data-ttu-id="b4be5-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="b4be5-129">**visPLOSplit**</span></span> <br/> |
   

