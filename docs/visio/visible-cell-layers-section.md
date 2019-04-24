---
title: Zelle "Visible" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357813"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="c42d5-103">Zelle "Visible" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="c42d5-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="c42d5-104">Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="c42d5-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="c42d5-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c42d5-105">**Value**</span></span>|<span data-ttu-id="c42d5-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c42d5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c42d5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c42d5-107">TRUE</span></span>  <br/> |<span data-ttu-id="c42d5-108">Shapes sind sichtbar.</span><span class="sxs-lookup"><span data-stu-id="c42d5-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="c42d5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c42d5-109">FALSE</span></span>  <br/> |<span data-ttu-id="c42d5-110">Shapes sind verborgen.</span><span class="sxs-lookup"><span data-stu-id="c42d5-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c42d5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c42d5-111">Remarks</span></span>

<span data-ttu-id="c42d5-112">Diese Zelle entspricht der Option **Visible** im Dialogfeld **Layereigenschaften** (Klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften** ).</span><span class="sxs-lookup"><span data-stu-id="c42d5-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="c42d5-113">Wenn Sie einen Verweis auf die Zelle Visible aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c42d5-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c42d5-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c42d5-114">Cell name:</span></span>  <br/> |<span data-ttu-id="c42d5-115">Layers. Visible [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c42d5-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c42d5-116">Wenn Sie einen Verweis auf die Zelle Visible aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c42d5-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c42d5-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c42d5-117">Section index:</span></span>  <br/> |<span data-ttu-id="c42d5-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="c42d5-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="c42d5-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c42d5-119">Row index:</span></span>  <br/> |<span data-ttu-id="c42d5-120">**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c42d5-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c42d5-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c42d5-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c42d5-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="c42d5-122">**visLayerVisible**</span></span> <br/> |
   

