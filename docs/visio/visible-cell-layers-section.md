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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405450"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="54fa5-103">Zelle "Visible" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="54fa5-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="54fa5-104">Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="54fa5-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="54fa5-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="54fa5-105">**Value**</span></span>|<span data-ttu-id="54fa5-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="54fa5-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="54fa5-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="54fa5-107">TRUE</span></span>  <br/> |<span data-ttu-id="54fa5-108">Shapes sind sichtbar.</span><span class="sxs-lookup"><span data-stu-id="54fa5-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="54fa5-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="54fa5-109">FALSE</span></span>  <br/> |<span data-ttu-id="54fa5-110">Shapes sind verborgen.</span><span class="sxs-lookup"><span data-stu-id="54fa5-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="54fa5-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54fa5-111">Remarks</span></span>

<span data-ttu-id="54fa5-112">Diese Zelle entspricht der Option **Visible** im Dialogfeld **Layereigenschaften** (klicken  Sie auf der Registerkarte **Start** in der Gruppe Bearbeiten auf **Ebenen,** und klicken Sie dann auf **Layereigenschaften** ).</span><span class="sxs-lookup"><span data-stu-id="54fa5-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="54fa5-113">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Visible anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="54fa5-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54fa5-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="54fa5-114">Cell name:</span></span>  <br/> |<span data-ttu-id="54fa5-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="54fa5-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="54fa5-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Visible nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="54fa5-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="54fa5-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="54fa5-117">Section index:</span></span>  <br/> |<span data-ttu-id="54fa5-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="54fa5-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="54fa5-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="54fa5-119">Row index:</span></span>  <br/> |<span data-ttu-id="54fa5-120">**visRowLayer**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="54fa5-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="54fa5-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="54fa5-121">Cell index:</span></span>  <br/> |<span data-ttu-id="54fa5-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="54fa5-122">**visLayerVisible**</span></span> <br/> |
   

