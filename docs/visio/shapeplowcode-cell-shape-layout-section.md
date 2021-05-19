---
title: Zelle "ShapePlowCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423895"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a><span data-ttu-id="c4a62-103">Zelle "ShapePlowCode" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="c4a62-103">ShapePlowCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="c4a62-104">Legt fest, ob dieses platzierbare Shape verschoben wird, wenn Sie ein anderes platzierbares Shape in der Nähe dieses Shapes auf dem Zeichenblatt ablegen.</span><span class="sxs-lookup"><span data-stu-id="c4a62-104">Determines whether this placeable shape moves away when you drop another placeable shape near this shape on the drawing page.</span></span>
  
|<span data-ttu-id="c4a62-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c4a62-105">**Value**</span></span>|<span data-ttu-id="c4a62-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4a62-106">**Description**</span></span>|<span data-ttu-id="c4a62-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="c4a62-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c4a62-108">0</span><span class="sxs-lookup"><span data-stu-id="c4a62-108">0</span></span>  <br/> |<span data-ttu-id="c4a62-109">Verschieben nach Blattvorgabe.</span><span class="sxs-lookup"><span data-stu-id="c4a62-109">Plow as page specifies.</span></span>  <br/> |<span data-ttu-id="c4a62-110">**visSLOPlowDefault**</span><span class="sxs-lookup"><span data-stu-id="c4a62-110">**visSLOPlowDefault**</span></span> <br/> |
|<span data-ttu-id="c4a62-111">1</span><span class="sxs-lookup"><span data-stu-id="c4a62-111">1</span></span>  <br/> |<span data-ttu-id="c4a62-112">Keine Shapes verschieben.</span><span class="sxs-lookup"><span data-stu-id="c4a62-112">Plow no shapes.</span></span>  <br/> |<span data-ttu-id="c4a62-113">**visSLOPlowNever**</span><span class="sxs-lookup"><span data-stu-id="c4a62-113">**visSLOPlowNever**</span></span> <br/> |
|<span data-ttu-id="c4a62-114">2</span><span class="sxs-lookup"><span data-stu-id="c4a62-114">2</span></span>  <br/> |<span data-ttu-id="c4a62-115">Jedes Shape verschieben.</span><span class="sxs-lookup"><span data-stu-id="c4a62-115">Plow every shape.</span></span>  <br/> |<span data-ttu-id="c4a62-116">**visSLOPlowAlways**</span><span class="sxs-lookup"><span data-stu-id="c4a62-116">**visSLOPlowAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4a62-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4a62-117">Remarks</span></span>

<span data-ttu-id="c4a62-118">Sie können den Wert dieser Zelle für eine bestimmte Form auch auf der Registerkarte Platzierung [](run-in-developer-mode-display-the-developer-tab.md) im Dialogfeld Verhalten festlegen (wenn eine Form ausgewählt  ist, klicken Sie auf der Registerkarte Entwickler in der Gruppe **Shape-Entwurf** auf  **Verhalten,** und klicken Sie dann auf die Registerkarte Platzierung). </span><span class="sxs-lookup"><span data-stu-id="c4a62-118">You can also set the value of this cell for a particular shape on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="c4a62-119">Verwenden Sie zum Festlegen dieses Verhaltens für  *alle*  Formen auf dem Zeichenblatt die Zelle PlowCode im Abschnitt Seitenlayout.</span><span class="sxs-lookup"><span data-stu-id="c4a62-119">To set this behavior for  *all*  the shapes on the drawing page, use the PlowCode cell in the Page Layout section.</span></span> 
  
<span data-ttu-id="c4a62-120">Um einen Verweis auf die Zelle ShapePlowCode anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="c4a62-120">To get a reference to the ShapePlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4a62-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c4a62-121">Cell name:</span></span>  <br/> |<span data-ttu-id="c4a62-122">ShapePlowCode</span><span class="sxs-lookup"><span data-stu-id="c4a62-122">ShapePlowCode</span></span>  <br/> |
   
<span data-ttu-id="c4a62-123">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapePlowCode nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c4a62-123">To get a reference to the ShapePlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4a62-124">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c4a62-124">Section index:</span></span>  <br/> |<span data-ttu-id="c4a62-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c4a62-125">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c4a62-126">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c4a62-126">Row index:</span></span>  <br/> |<span data-ttu-id="c4a62-127">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="c4a62-127">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="c4a62-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c4a62-128">Cell index:</span></span>  <br/> |<span data-ttu-id="c4a62-129">**visSLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="c4a62-129">**visSLOPlowCode**</span></span> <br/> |
   

