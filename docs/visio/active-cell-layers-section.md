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
ms.openlocfilehash: f97f7dc09d1f882452ae2234882de45f06bd0da1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417434"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="a255b-104">Zelle "Active" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="a255b-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="a255b-p102">Gibt an, ob der Layer aktiv ist. Shapes ohne vorher zugewiesene Layer werden dem bzw. den aktiven Layern zugewiesen, wenn Sie sie auf das Zeichenblatt ziehen.</span><span class="sxs-lookup"><span data-stu-id="a255b-p102">Specifies whether the layer is active. Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="a255b-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a255b-107">**Value**</span></span>|<span data-ttu-id="a255b-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a255b-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a255b-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="a255b-109">TRUE</span></span>  <br/> |<span data-ttu-id="a255b-110">Layer ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="a255b-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="a255b-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="a255b-111">FALSE</span></span>  <br/> |<span data-ttu-id="a255b-112">Layer ist nicht aktiv.</span><span class="sxs-lookup"><span data-stu-id="a255b-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a255b-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a255b-113">Remarks</span></span>

<span data-ttu-id="a255b-114">Der Wert dieser Zelle entspricht der Einstellung **Aktiv** im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**).</span><span class="sxs-lookup"><span data-stu-id="a255b-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="a255b-115">Wenn Sie einen Verweis auf die aktive Zelle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a255b-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a255b-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a255b-116">Cell name:</span></span>  <br/> |<span data-ttu-id="a255b-117">Layers. Active [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="a255b-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="a255b-118">Wenn Sie einen Verweis auf die aktive Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a255b-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a255b-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a255b-119">Section index:</span></span>  <br/> |<span data-ttu-id="a255b-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="a255b-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="a255b-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a255b-121">Row index:</span></span>  <br/> |<span data-ttu-id="a255b-122">**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a255b-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a255b-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a255b-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a255b-124">**visLayerActive**</span><span class="sxs-lookup"><span data-stu-id="a255b-124">**visLayerActive**</span></span> <br/> |
   

