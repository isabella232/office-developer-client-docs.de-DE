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
ms.openlocfilehash: 81a54bebaa8ca68a8fbc8853c69f88efb34bbdb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797094"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="977aa-103">Glue Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="977aa-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="977aa-104">Gibt an, ob die dem Layer zugehörigen Shapes geklebt werden können.</span><span class="sxs-lookup"><span data-stu-id="977aa-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="977aa-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="977aa-105">**Value**</span></span>|<span data-ttu-id="977aa-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="977aa-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="977aa-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="977aa-107">TRUE</span></span>  <br/> |<span data-ttu-id="977aa-108">Klebefunktion ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="977aa-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="977aa-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="977aa-109">FALSE</span></span>  <br/> |<span data-ttu-id="977aa-110">Klebefunktion ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="977aa-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="977aa-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="977aa-111">Remarks</span></span>

<span data-ttu-id="977aa-112">Diese Zelle entspricht der Option **Kleben** im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** , klicken Sie auf **Ebenen**, und klicken Sie dann auf **Layereigenschaften** ).</span><span class="sxs-lookup"><span data-stu-id="977aa-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="977aa-113">Wenn Sie einen Verweis auf die Zelle Glue aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="977aa-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="977aa-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="977aa-114">Cell name:</span></span>  <br/> |<span data-ttu-id="977aa-115">Layers.Glue [ *i* ] wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="977aa-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="977aa-116">Wenn Sie einen Verweis auf die Zelle Glue aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="977aa-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="977aa-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="977aa-117">Section index:</span></span>  <br/> |<span data-ttu-id="977aa-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="977aa-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="977aa-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="977aa-119">Row index:</span></span>  <br/> |<span data-ttu-id="977aa-120">**VisRowLayer** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="977aa-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="977aa-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="977aa-121">Cell index:</span></span>  <br/> |<span data-ttu-id="977aa-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="977aa-122">**visLayerGlue**</span></span> <br/> |
   

