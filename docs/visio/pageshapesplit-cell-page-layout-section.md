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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301484"
---
# <a name="pageshapesplit-cell-page-layout-section"></a><span data-ttu-id="70d40-103">Zelle "PageShapeSplit" (Abschnitt "Page Layout")</span><span class="sxs-lookup"><span data-stu-id="70d40-103">PageShapeSplit Cell (Page Layout Section)</span></span>

<span data-ttu-id="70d40-104">Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.</span><span class="sxs-lookup"><span data-stu-id="70d40-104">Indicates whether shapes on the page can be automatically split.</span></span>
  
|<span data-ttu-id="70d40-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="70d40-105">**Value**</span></span>|<span data-ttu-id="70d40-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="70d40-106">**Description**</span></span>|<span data-ttu-id="70d40-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="70d40-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="70d40-108">0</span><span class="sxs-lookup"><span data-stu-id="70d40-108">0</span></span>  <br/> |<span data-ttu-id="70d40-109">Automatische Shape-Teilung nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="70d40-109">Do not allow automatic shape splitting.</span></span>  <br/> |<span data-ttu-id="70d40-110">**visPLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="70d40-110">**visPLOSplitNone**</span></span> <br/> |
|<span data-ttu-id="70d40-111">1</span><span class="sxs-lookup"><span data-stu-id="70d40-111">1</span></span>  <br/> |<span data-ttu-id="70d40-112">Automatische Shape-Teilung zulassen (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="70d40-112">Allow automatic shape splitting (the default).</span></span>  <br/> |<span data-ttu-id="70d40-113">**visPLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="70d40-113">**visPLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="70d40-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70d40-114">Remarks</span></span>

<span data-ttu-id="70d40-p101">Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. Die Standardeinstellungen für Shapes hängen vom Typ der Zeichnung ab.</span><span class="sxs-lookup"><span data-stu-id="70d40-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page levels. The default setting for shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="70d40-118">Um die Aufteilung auf Anwendungsebene zu aktivieren oder zu deaktivieren, verwenden Sie die Einstellung **Verbindungs Aufteilung aktivieren** auf der Registerkarte **erweitert** des Dialogfelds **Visio-Optionen** (Klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf der **Visio** -Seite auf **Optionen** . , und klicken Sie dann auf **erweitert** ).</span><span class="sxs-lookup"><span data-stu-id="70d40-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **Office** button, click **Options** on the **Visio** tab, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="70d40-119">Informationen zum Aktivieren oder Deaktivieren der Aufteilung auf Shape-Ebene finden Sie in den Zellen ShapeSplit und ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="70d40-119">To enable or disable splitting at the shape level, see the ShapeSplit and ShapeSplittable cells.</span></span> 
  
<span data-ttu-id="70d40-120">Wenn Sie einen Verweis auf die Zelle PageShapeSplit aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="70d40-120">To get a reference to the PageShapeSplit cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70d40-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="70d40-121">Cell name:</span></span>  <br/> |<span data-ttu-id="70d40-122">PageShapeSplit</span><span class="sxs-lookup"><span data-stu-id="70d40-122">PageShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="70d40-123">Wenn Sie einen Verweis auf die Zelle PageShapeSplit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="70d40-123">To get a reference to the PageShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="70d40-124">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="70d40-124">Section index:</span></span>  <br/> |<span data-ttu-id="70d40-125">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="70d40-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="70d40-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="70d40-126">Row index:</span></span>  <br/> |<span data-ttu-id="70d40-127">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="70d40-127">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="70d40-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="70d40-128">Cell index:</span></span>  <br/> |<span data-ttu-id="70d40-129">**visPLOSplit**</span><span class="sxs-lookup"><span data-stu-id="70d40-129">**visPLOSplit**</span></span> <br/> |
   

