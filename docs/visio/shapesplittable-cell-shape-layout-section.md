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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349154"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="5ba43-103">Zelle "ShapeSplittable" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="5ba43-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="5ba43-104">Zeigt an, ob dieses 1D-Shape geteilt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5ba43-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="5ba43-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5ba43-105">**Value**</span></span>|<span data-ttu-id="5ba43-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5ba43-106">**Description**</span></span>|<span data-ttu-id="5ba43-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="5ba43-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="5ba43-108">0</span><span class="sxs-lookup"><span data-stu-id="5ba43-108">0</span></span>  <br/> | <span data-ttu-id="5ba43-109">Teilen des Shapes nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="5ba43-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="5ba43-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="5ba43-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="5ba43-111">1</span><span class="sxs-lookup"><span data-stu-id="5ba43-111">1</span></span>  <br/> | <span data-ttu-id="5ba43-112">Teilen des Shapes zulassen.</span><span class="sxs-lookup"><span data-stu-id="5ba43-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="5ba43-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="5ba43-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ba43-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ba43-114">Remarks</span></span>

<span data-ttu-id="5ba43-115">Das Standardverhalten von Verbindern und anderen 1D-Shapes hängt vom Zeichnungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="5ba43-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="5ba43-p101">Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5ba43-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="5ba43-118">Um die Aufteilung auf Anwendungsebene zu aktivieren oder zu deaktivieren, verwenden Sie die Einstellung **Verbinder-Aufteilung aktivieren** auf der Registerkarte **erweitert** des Dialogfelds **Visio-Optionen** (Klicken Sie auf die Registerkarte **Datei** , dann auf **Optionen**und dann auf \*\* Advanced\*\* ).</span><span class="sxs-lookup"><span data-stu-id="5ba43-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="5ba43-119">Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle [PageShapeSplit](pageshapesplit-cell-page-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="5ba43-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="5ba43-120">Wenn Sie ein Shape so konfigurieren möchten, dass es teilbare 1D-Shapes teilt, lesen Sie die Informationen zur Zelle [ShapeSplit](shapesplit-cell-shape-layout-section.md).</span><span class="sxs-lookup"><span data-stu-id="5ba43-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="5ba43-121">Wenn Sie einen Verweis auf die Zelle ShapeSplittable aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5ba43-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ba43-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5ba43-122">Cell name:</span></span>  <br/> | <span data-ttu-id="5ba43-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="5ba43-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="5ba43-124">Wenn Sie einen Verweis auf die Zelle ShapeSplittable aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5ba43-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ba43-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5ba43-125">Section index:</span></span>  <br/> |<span data-ttu-id="5ba43-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5ba43-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5ba43-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5ba43-127">Row index:</span></span>  <br/> |<span data-ttu-id="5ba43-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="5ba43-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="5ba43-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5ba43-129">Cell index:</span></span>  <br/> |<span data-ttu-id="5ba43-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="5ba43-130">**visSLOSplittable**</span></span> <br/> |
   

