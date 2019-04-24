---
title: Zelle "ShapeSplit" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Gibt an, ob dieses Shape andere Shapes teilen kann, sofern diese teilbar sind.
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349119"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="98cc9-103">Zelle "ShapeSplit" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="98cc9-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="98cc9-104">Gibt an, ob dieses Shape andere Shapes teilen kann, sofern diese teilbar sind.</span><span class="sxs-lookup"><span data-stu-id="98cc9-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="98cc9-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="98cc9-105">**Value**</span></span>|<span data-ttu-id="98cc9-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="98cc9-106">**Description**</span></span>|<span data-ttu-id="98cc9-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="98cc9-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="98cc9-108">0</span><span class="sxs-lookup"><span data-stu-id="98cc9-108">0</span></span>  <br/> | <span data-ttu-id="98cc9-109">Teilen anderer Shapes durch dieses Shape nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="98cc9-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="98cc9-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="98cc9-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="98cc9-111">1</span><span class="sxs-lookup"><span data-stu-id="98cc9-111">1</span></span>  <br/> | <span data-ttu-id="98cc9-112">Teilen anderer Shapes durch dieses Shape zulassen.</span><span class="sxs-lookup"><span data-stu-id="98cc9-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="98cc9-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="98cc9-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="98cc9-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98cc9-114">Remarks</span></span>

<span data-ttu-id="98cc9-115">Ein Shape, das andere Shapes teilen kann, muss entweder ein 2D-Shape oder ein platzierbares 1D-Shape sein.</span><span class="sxs-lookup"><span data-stu-id="98cc9-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="98cc9-p101">Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert, bei Shapes hängt es vom Zeichnungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="98cc9-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="98cc9-118">Um die Aufteilung auf Anwendungsebene zu aktivieren oder zu deaktivieren, verwenden Sie die Einstellung **Verbinder-Aufteilung aktivieren** auf der Registerkarte **erweitert** des Dialogfelds **Visio-Optionen** (Klicken Sie auf die Registerkarte **Datei** , dann auf **Optionen**und dann auf \*\* Advanced\*\*).</span><span class="sxs-lookup"><span data-stu-id="98cc9-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="98cc9-119">Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle PageShapeSplit.</span><span class="sxs-lookup"><span data-stu-id="98cc9-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="98cc9-120">Wenn Sie ein 1D-Shape teilbar machen möchten, lesen Sie die Informationen zur Zelle ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="98cc9-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="98cc9-121">Wenn Sie einen Verweis auf die Zelle ShapeSplit aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="98cc9-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="98cc9-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="98cc9-122">Cell name:</span></span>  <br/> | <span data-ttu-id="98cc9-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="98cc9-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="98cc9-124">Wenn Sie einen Verweis auf die Zelle ShapeSplit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="98cc9-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="98cc9-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="98cc9-125">Section index:</span></span>  <br/> |<span data-ttu-id="98cc9-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="98cc9-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="98cc9-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="98cc9-127">Row index:</span></span>  <br/> |<span data-ttu-id="98cc9-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="98cc9-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="98cc9-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="98cc9-129">Cell index:</span></span>  <br/> |<span data-ttu-id="98cc9-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="98cc9-130">**visSLOSplit**</span></span> <br/> |
   

