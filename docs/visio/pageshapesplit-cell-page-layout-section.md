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
ms.openlocfilehash: 7f1df0158cde6853c5518597c853cb56151eefbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797599"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="e4ea7-103">PageShapeSplit Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="e4ea7-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="e4ea7-104">Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="e4ea7-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e4ea7-105">**Value**</span></span>|<span data-ttu-id="e4ea7-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e4ea7-106">**Description**</span></span>|<span data-ttu-id="e4ea7-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="e4ea7-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e4ea7-108">0</span><span class="sxs-lookup"><span data-stu-id="e4ea7-108">0</span></span>  <br/> |<span data-ttu-id="e4ea7-109">Automatische Shape-Teilung nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="e4ea7-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="e4ea7-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="e4ea7-111">1</span><span class="sxs-lookup"><span data-stu-id="e4ea7-111">1</span></span>  <br/> |<span data-ttu-id="e4ea7-112">Automatische Shape-Teilung zulassen (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="e4ea7-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="e4ea7-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="e4ea7-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e4ea7-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e4ea7-114">Remarks</span></span>

<span data-ttu-id="e4ea7-p101">Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. Die Standardeinstellungen für Shapes hängen vom Typ der Zeichnung ab.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page levels. The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="e4ea7-118">Zum Aktivieren oder Deaktivieren des Teilens auf Anwendungsebene, verwenden Sie die Einstellung **Connector aufteilen aktivieren** auf der Registerkarte **Erweitert** im Dialogfeld **Visio-Optionen** (klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf der **Visio** - **Optionen** Registerkarte, und klicken Sie dann auf **Erweitert** ).</span><span class="sxs-lookup"><span data-stu-id="e4ea7-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="e4ea7-119">Zum Aktivieren oder Deaktivieren des Teilens auf Shape-Ebene, finden Sie in den Zellen ShapeSplit und ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="e4ea7-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="e4ea7-120">Wenn Sie einen Verweis auf die Zelle PageShapeSplit nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e4ea7-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4ea7-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e4ea7-121">Cell name:</span></span>  <br/> |<span data-ttu-id="e4ea7-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="e4ea7-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="e4ea7-123">Wenn Sie einen Verweis auf die Zelle PageShapeSplit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e4ea7-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e4ea7-124">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e4ea7-124">Section index:</span></span>  <br/> |<span data-ttu-id="e4ea7-125">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e4ea7-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e4ea7-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e4ea7-126">Row index:</span></span>  <br/> |<span data-ttu-id="e4ea7-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e4ea7-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="e4ea7-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e4ea7-128">Cell index:</span></span>  <br/> |<span data-ttu-id="e4ea7-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="e4ea7-129">**visPLOSplit**</span></span> <br/> |
   

