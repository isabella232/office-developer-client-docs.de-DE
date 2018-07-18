---
title: Zelle "Active" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Gibt an, ob der Layer aktiv ist. Shapes ohne vorher zugewiesene Layer werden dem bzw. den aktiven Layern zugewiesen, wenn Sie sie auf das Zeichenblatt ziehen.
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796381"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="6b5e7-104">Active Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="6b5e7-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="6b5e7-p102">Gibt an, ob der Layer aktiv ist. Shapes ohne vorher zugewiesene Layer werden dem bzw. den aktiven Layern zugewiesen, wenn Sie sie auf das Zeichenblatt ziehen.</span><span class="sxs-lookup"><span data-stu-id="6b5e7-p102">Specifies whether the layer is active. Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="6b5e7-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6b5e7-107">**Value**</span></span>|<span data-ttu-id="6b5e7-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6b5e7-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6b5e7-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="6b5e7-109">TRUE</span></span>  <br/> |<span data-ttu-id="6b5e7-110">
          Layer ist aktiv.
</span><span class="sxs-lookup"><span data-stu-id="6b5e7-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="6b5e7-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="6b5e7-111">FALSE</span></span>  <br/> |<span data-ttu-id="6b5e7-112">
          Layer ist nicht aktiv.
</span><span class="sxs-lookup"><span data-stu-id="6b5e7-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6b5e7-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b5e7-113">Remarks</span></span>

<span data-ttu-id="6b5e7-114">Der Wert dieser Zelle entspricht der Einstellung **Aktiv** im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="6b5e7-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="6b5e7-115">Wenn Sie einen Verweis auf die Zelle Active aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6b5e7-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b5e7-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6b5e7-116">Cell name:</span></span>  <br/> |<span data-ttu-id="6b5e7-117">Layers.Active [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6b5e7-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6b5e7-118">Wenn Sie einen Verweis auf die Zelle Active aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6b5e7-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6b5e7-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6b5e7-119">Section index:</span></span>  <br/> |<span data-ttu-id="6b5e7-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="6b5e7-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="6b5e7-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6b5e7-121">Row index:</span></span>  <br/> |<span data-ttu-id="6b5e7-122">**VisRowLayer** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6b5e7-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6b5e7-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6b5e7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="6b5e7-124">**visLayerActive**</span><span class="sxs-lookup"><span data-stu-id="6b5e7-124">**visLayerActive**</span></span> <br/> |
   

