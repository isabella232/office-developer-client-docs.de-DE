---
title: Zelle "Glue" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Gibt an, ob die dem Layer zugehörigen Shapes geklebt werden können.
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408516"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="86ed9-103">Zelle "Glue" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="86ed9-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="86ed9-104">Gibt an, ob die dem Layer zugehörigen Shapes geklebt werden können.</span><span class="sxs-lookup"><span data-stu-id="86ed9-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="86ed9-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="86ed9-105">**Value**</span></span>|<span data-ttu-id="86ed9-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86ed9-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="86ed9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="86ed9-107">TRUE</span></span>  <br/> |<span data-ttu-id="86ed9-108">Klebefunktion ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="86ed9-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="86ed9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="86ed9-109">FALSE</span></span>  <br/> |<span data-ttu-id="86ed9-110">Klebefunktion ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="86ed9-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="86ed9-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="86ed9-111">Remarks</span></span>

<span data-ttu-id="86ed9-112">Diese Zelle entspricht der Option  **Kleben** im Dialogfeld Layereigenschaften (klicken Sie auf der Registerkarte **Start** in der Gruppe Bearbeiten auf **Ebenen,** und klicken Sie dann auf **Layereigenschaften** ). </span><span class="sxs-lookup"><span data-stu-id="86ed9-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="86ed9-113">Um einen Verweis auf die Zelle Glue anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="86ed9-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86ed9-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="86ed9-114">Cell name:</span></span>  <br/> |<span data-ttu-id="86ed9-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="86ed9-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="86ed9-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Glue nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="86ed9-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="86ed9-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="86ed9-117">Section index:</span></span>  <br/> |<span data-ttu-id="86ed9-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="86ed9-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="86ed9-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="86ed9-119">Row index:</span></span>  <br/> |<span data-ttu-id="86ed9-120">**visRowLayer**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="86ed9-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="86ed9-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="86ed9-121">Cell index:</span></span>  <br/> |<span data-ttu-id="86ed9-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="86ed9-122">**visLayerGlue**</span></span> <br/> |
   

