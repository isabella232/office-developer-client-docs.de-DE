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
ms.openlocfilehash: b782977bd5b7e828223675eb16f4e7e48f4ca55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798051"
---
# <a name="shapesplit-cell-shape-layout-section"></a><span data-ttu-id="ddfe8-103">ShapeSplit Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="ddfe8-103">ShapeSplit Cell (Shape Layout Section)</span></span>

<span data-ttu-id="ddfe8-104">Gibt an, ob dieses Shape andere Shapes teilen kann, sofern diese teilbar sind.</span><span class="sxs-lookup"><span data-stu-id="ddfe8-104">Indicates whether this shape can split shapes that are splittable.</span></span>
  
|<span data-ttu-id="ddfe8-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ddfe8-105">**Value**</span></span>|<span data-ttu-id="ddfe8-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ddfe8-106">**Description**</span></span>|<span data-ttu-id="ddfe8-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="ddfe8-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="ddfe8-108">0</span><span class="sxs-lookup"><span data-stu-id="ddfe8-108">0</span></span>  <br/> | <span data-ttu-id="ddfe8-109">Teilen anderer Shapes durch dieses Shape nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="ddfe8-109">Do not allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="ddfe8-110">**visSLOSplitNone**</span><span class="sxs-lookup"><span data-stu-id="ddfe8-110">**visSLOSplitNone**</span></span> <br/> |
| <span data-ttu-id="ddfe8-111">1</span><span class="sxs-lookup"><span data-stu-id="ddfe8-111">1</span></span>  <br/> | <span data-ttu-id="ddfe8-112">Teilen anderer Shapes durch dieses Shape zulassen.</span><span class="sxs-lookup"><span data-stu-id="ddfe8-112">Allow this shape to split other shapes.</span></span>  <br/> |<span data-ttu-id="ddfe8-113">**visSLOSplitAllow**</span><span class="sxs-lookup"><span data-stu-id="ddfe8-113">**visSLOSplitAllow**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ddfe8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddfe8-114">Remarks</span></span>

<span data-ttu-id="ddfe8-115">Ein Shape, das andere Shapes teilen kann, muss entweder ein 2D-Shape oder ein platzierbares 1D-Shape sein.</span><span class="sxs-lookup"><span data-stu-id="ddfe8-115">A shape that can split other shapes must be either a 2-D shape or a 1-D placeable shape.</span></span> 
  
<span data-ttu-id="ddfe8-p101">Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert, bei Shapes hängt es vom Zeichnungstyp ab.</span><span class="sxs-lookup"><span data-stu-id="ddfe8-p101">Automatic splitting of shapes is enabled and disabled at three different levels: application, page, and shape. By default, splitting is enabled at the application and page level; for shapes, it varies by drawing type.</span></span> 
  
<span data-ttu-id="ddfe8-118">Zum Aktivieren oder Deaktivieren des Teilens auf Anwendungsebene, verwenden Sie die Einstellung **Connector aufteilen aktivieren** auf der Registerkarte **Erweitert** im Dialogfeld **Visio-Optionen** (klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Optionen**, und klicken Sie dann auf ** Erweiterte**).</span><span class="sxs-lookup"><span data-stu-id="ddfe8-118">To enable or disable splitting at the application level, use the **Enable connector splitting** setting on the **Advanced** tab of the **Visio Options** dialog box (click the **File** tab, click **Options**, and then click **Advanced**).</span></span> 
  
<span data-ttu-id="ddfe8-119">Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle PageShapeSplit.</span><span class="sxs-lookup"><span data-stu-id="ddfe8-119">To enable or disable splitting on a page, see the PageShapeSplit cell.</span></span> 
  
<span data-ttu-id="ddfe8-120">Wenn Sie ein 1D-Shape teilbar machen möchten, lesen Sie die Informationen zur Zelle ShapeSplittable.</span><span class="sxs-lookup"><span data-stu-id="ddfe8-120">To cause a 1-D shape to be splittable, see the ShapeSplittable cell.</span></span>
  
<span data-ttu-id="ddfe8-121">Zum Abrufen eines Verweises auf die Zelle ShapeSplit nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ddfe8-121">To get a reference to the ShapeSplit cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddfe8-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ddfe8-122">Cell name:</span></span>  <br/> | <span data-ttu-id="ddfe8-123">ShapeSplit</span><span class="sxs-lookup"><span data-stu-id="ddfe8-123">ShapeSplit</span></span>  <br/> |
   
<span data-ttu-id="ddfe8-124">Wenn Sie einen Verweis auf die Zelle ShapeSplit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ddfe8-124">To get a reference to the ShapeSplit cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ddfe8-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ddfe8-125">Section index:</span></span>  <br/> |<span data-ttu-id="ddfe8-126">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ddfe8-126">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ddfe8-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ddfe8-127">Row index:</span></span>  <br/> |<span data-ttu-id="ddfe8-128">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="ddfe8-128">**visRowShapeLayout**</span></span> <br/> |
| <span data-ttu-id="ddfe8-129">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ddfe8-129">Cell index:</span></span>  <br/> |<span data-ttu-id="ddfe8-130">**visSLOSplit**</span><span class="sxs-lookup"><span data-stu-id="ddfe8-130">**visSLOSplit**</span></span> <br/> |
   

