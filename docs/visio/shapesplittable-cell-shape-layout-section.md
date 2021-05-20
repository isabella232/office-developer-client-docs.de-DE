---
title: Zelle "ShapeSplittable" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Zeigt an, ob dieses 1D-Shape geteilt werden kann.
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427073"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="2c46f-103">Zelle "ShapeSplittable" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="2c46f-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="2c46f-104">Zeigt an, ob dieses 1D-Shape geteilt werden kann.</span><span class="sxs-lookup"><span data-stu-id="2c46f-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="2c46f-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2c46f-105">**Value**</span></span>|<span data-ttu-id="2c46f-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c46f-106">**Description**</span></span>|<span data-ttu-id="2c46f-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="2c46f-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2c46f-108">0</span><span class="sxs-lookup"><span data-stu-id="2c46f-108">0</span></span>  <br/> | <span data-ttu-id="2c46f-109">Teilen des Shapes nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="2c46f-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="2c46f-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="2c46f-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="2c46f-111">1</span><span class="sxs-lookup"><span data-stu-id="2c46f-111">1</span></span>  <br/> | <span data-ttu-id="2c46f-112">Teilen des Shapes zulassen.</span><span class="sxs-lookup"><span data-stu-id="2c46f-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="2c46f-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="2c46f-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c46f-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c46f-114">Remarks</span></span>

<span data-ttu-id="2c46f-115">Das Standardverhalten von Verbindern und anderen 1D-Shapes hängt vom Zeichnungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="2c46f-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="2c46f-p101">Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="2c46f-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="2c46f-118">Verwenden Sie zum Aktivieren oder Deaktivieren der  Aufteilung auf Anwendungsebene  die Einstellung Connectorteilung aktivieren auf der  Registerkarte Erweitert im Dialogfeld **Visio-Optionen** (klicken Sie auf die Registerkarte Datei, klicken Sie auf **Optionen** und dann auf **Erweitert** ).</span><span class="sxs-lookup"><span data-stu-id="2c46f-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="2c46f-119">Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle [PageShapeSplit](pageshapesplit-cell-page-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="2c46f-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="2c46f-120">Wenn Sie ein Shape so konfigurieren möchten, dass es teilbare 1D-Shapes teilt, lesen Sie die Informationen zur Zelle [ShapeSplit](shapesplit-cell-shape-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="2c46f-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="2c46f-121">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ShapeSplittable anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="2c46f-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c46f-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2c46f-122">Cell name:</span></span>  <br/> | <span data-ttu-id="2c46f-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="2c46f-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="2c46f-124">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeSplittable nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2c46f-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c46f-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2c46f-125">Section index:</span></span>  <br/> |<span data-ttu-id="2c46f-126">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2c46f-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2c46f-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2c46f-127">Row index:</span></span>  <br/> |<span data-ttu-id="2c46f-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="2c46f-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="2c46f-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2c46f-129">Cell index:</span></span>  <br/> |<span data-ttu-id="2c46f-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="2c46f-130">**visSLOSplittable**</span></span> <br/> |
   

