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
ms.openlocfilehash: e2db881465a19b34d5788f1621f15c4d7d15c293
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798058"
---
# <a name="shapesplittable-cell-shape-layout-section"></a><span data-ttu-id="ddb33-103">ShapeSplittable Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="ddb33-103">ShapeSplittable Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ddb33-104">Zeigt an, ob dieses 1D-Shape geteilt werden kann.</span><span class="sxs-lookup"><span data-stu-id="ddb33-104">Indicates whether this 1-D shape can be split.</span></span> 
  
|<span data-ttu-id="ddb33-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ddb33-105">**Value**</span></span>|<span data-ttu-id="ddb33-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddb33-106">**Description**</span></span>|<span data-ttu-id="ddb33-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="ddb33-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ddb33-108">0</span><span class="sxs-lookup"><span data-stu-id="ddb33-108">0</span></span>  <br/> | <span data-ttu-id="ddb33-109">Teilen des Shapes nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="ddb33-109">Do not allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="ddb33-110">**visSLOSplittableNone**</span><span class="sxs-lookup"><span data-stu-id="ddb33-110">**visSLOSplittableNone**</span></span> <br/> |
| <span data-ttu-id="ddb33-111">1</span><span class="sxs-lookup"><span data-stu-id="ddb33-111">1</span></span>  <br/> | <span data-ttu-id="ddb33-112">Teilen des Shapes zulassen.</span><span class="sxs-lookup"><span data-stu-id="ddb33-112">Allow this shape to be split.</span></span>  <br/> |<span data-ttu-id="ddb33-113">**visSLOSplittableAllow**</span><span class="sxs-lookup"><span data-stu-id="ddb33-113">**visSLOSplittableAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddb33-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddb33-114">Remarks</span></span>

<span data-ttu-id="ddb33-115">Das Standardverhalten von Verbindern und anderen 1D-Shapes hängt vom Zeichnungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="ddb33-115">The default behavior for connectors and other 1-D shapes varies by drawing type.</span></span> 
  
<span data-ttu-id="ddb33-p101">Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ddb33-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application level and page levels.</span></span> 
  
<span data-ttu-id="ddb33-118">Zum Aktivieren oder Deaktivieren des Teilens auf Anwendungsebene, verwenden Sie die Einstellung **Connector aufteilen aktivieren** auf der Registerkarte **Erweitert** im Dialogfeld **Visio-Optionen** (klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Optionen**, und klicken Sie dann auf ** Erweiterte** ).</span><span class="sxs-lookup"><span data-stu-id="ddb33-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced** ).</span></span> 
  
<span data-ttu-id="ddb33-119">Zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt finden die Informationen zur Zelle [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb33-119">To enable or disable splitting on a page, see the [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="ddb33-120">Wenn ein Shape teilbare 1D-Shapes können, lesen Sie die Zelle [ShapeSplit](shapesplit-cell-shape-layout-section.md) .</span><span class="sxs-lookup"><span data-stu-id="ddb33-120">To cause a shape to be able to split 1-D splittable shapes, see the [ShapeSplit](shapesplit-cell-shape-layout-section.md) cell.</span></span> 
  
<span data-ttu-id="ddb33-121">Zum Abrufen eines Verweises auf die Zelle ShapeSplittable nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ddb33-121">To get a reference to the ShapeSplittable cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddb33-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ddb33-122">Cell name:</span></span>  <br/> | <span data-ttu-id="ddb33-123">ShapeSplittable</span><span class="sxs-lookup"><span data-stu-id="ddb33-123">ShapeSplittable</span></span>  <br/> |
   
<span data-ttu-id="ddb33-124">Wenn Sie einen Verweis auf die Zelle ShapeSplittable aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ddb33-124">To get a reference to the ShapeSplittable cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddb33-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ddb33-125">Section index:</span></span>  <br/> |<span data-ttu-id="ddb33-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ddb33-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ddb33-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ddb33-127">Row index:</span></span>  <br/> |<span data-ttu-id="ddb33-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ddb33-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="ddb33-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ddb33-129">Cell index:</span></span>  <br/> |<span data-ttu-id="ddb33-130">**visSLOSplittable**</span><span class="sxs-lookup"><span data-stu-id="ddb33-130">**visSLOSplittable**</span></span> <br/> |
   

