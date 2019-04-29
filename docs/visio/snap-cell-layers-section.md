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
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434844"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="316e7-104">Zelle "Snap" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="316e7-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="316e7-p102">Bestimmt, ob andere Shapes an den dem Layer zugeordneten Shapes einrasten können. Die dem Layer zugeordneten Shapes können an anderen Shapes einrasten, andere Shapes jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="316e7-p102">Determines whether other shapes can snap to shapes assigned to the layer. Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="316e7-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="316e7-107">**Value**</span></span>|<span data-ttu-id="316e7-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="316e7-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="316e7-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="316e7-109">TRUE</span></span>  <br/> |<span data-ttu-id="316e7-110">Andere Shapes können an den dem Layer zugeordneten Shapes einrasten.</span><span class="sxs-lookup"><span data-stu-id="316e7-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="316e7-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="316e7-111">FALSE</span></span>  <br/> |<span data-ttu-id="316e7-112">Andere Shapes können an den dem Layer zugeordneten Shapes nicht einrasten.</span><span class="sxs-lookup"><span data-stu-id="316e7-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="316e7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="316e7-113">Remarks</span></span>

<span data-ttu-id="316e7-114">Sie können den Wert dieser Zelle auch über die Option **Ausrichten** im Dialogfeld **Layereigenschaften** festlegen (klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="316e7-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="316e7-115">Wenn Sie einen Verweis auf die Zelle "Snap" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="316e7-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="316e7-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="316e7-116">Cell name:</span></span>  <br/> |<span data-ttu-id="316e7-117">Layers. Snap [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="316e7-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="316e7-118">Wenn Sie einen Verweis auf die Zelle "Snap" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="316e7-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="316e7-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="316e7-119">Section index:</span></span>  <br/> |<span data-ttu-id="316e7-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="316e7-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="316e7-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="316e7-121">Row index:</span></span>  <br/> |<span data-ttu-id="316e7-122">**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="316e7-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="316e7-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="316e7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="316e7-124">**visLayerSnap**</span><span class="sxs-lookup"><span data-stu-id="316e7-124">**visLayerSnap**</span></span> <br/> |
   

