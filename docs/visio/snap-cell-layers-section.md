---
title: Zelle "Snap" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Bestimmt, ob andere Shapes an den dem Layer zugeordneten Shapes einrasten können. Die dem Layer zugeordneten Shapes können an anderen Shapes einrasten, andere Shapes jedoch nicht.
ms.openlocfilehash: 7fc684afb67d0454ea5907c08f4f7644d97c7f74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798137"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="31131-104">Snap Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="31131-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="31131-p102">Bestimmt, ob andere Shapes an den dem Layer zugeordneten Shapes einrasten können. Die dem Layer zugeordneten Shapes können an anderen Shapes einrasten, andere Shapes jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="31131-p102">Determines whether other shapes can snap to shapes assigned to the layer. Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="31131-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="31131-107">**Value**</span></span>|<span data-ttu-id="31131-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31131-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="31131-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="31131-109">TRUE</span></span>  <br/> |<span data-ttu-id="31131-110">Andere Shapes können an den dem Layer zugeordneten Shapes einrasten.</span><span class="sxs-lookup"><span data-stu-id="31131-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="31131-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="31131-111">FALSE</span></span>  <br/> |<span data-ttu-id="31131-112">Andere Shapes können an den dem Layer zugeordneten Shapes nicht einrasten.</span><span class="sxs-lookup"><span data-stu-id="31131-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31131-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31131-113">Remarks</span></span>

<span data-ttu-id="31131-114">Sie können den Wert dieser Zelle auch über die Option **Ausrichten** im Dialogfeld **Layereigenschaften** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="31131-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="31131-115">Wenn Sie einen Verweis auf die Zelle Snap aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="31131-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31131-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="31131-116">Cell name:</span></span>  <br/> |<span data-ttu-id="31131-117">Layers.Snap [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="31131-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="31131-118">Wenn Sie einen Verweis auf die Zelle Snap aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="31131-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="31131-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="31131-119">Section index:</span></span>  <br/> |<span data-ttu-id="31131-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="31131-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="31131-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="31131-121">Row index:</span></span>  <br/> |<span data-ttu-id="31131-122">**VisRowLayer** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="31131-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="31131-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="31131-123">Cell index:</span></span>  <br/> |<span data-ttu-id="31131-124">**visLayerSnap**</span><span class="sxs-lookup"><span data-stu-id="31131-124">**visLayerSnap**</span></span> <br/> |
   

