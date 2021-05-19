---
title: Zelle "Print" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Gibt an, ob die dem Layer zugehörigen Shapes ausgedruckt werden können.
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435215"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="4de9e-103">Zelle "Print" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="4de9e-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="4de9e-104">Gibt an, ob die dem Layer zugehörigen Shapes ausgedruckt werden können.</span><span class="sxs-lookup"><span data-stu-id="4de9e-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="4de9e-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4de9e-105">**Value**</span></span>|<span data-ttu-id="4de9e-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4de9e-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4de9e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4de9e-107">TRUE</span></span>  <br/> |<span data-ttu-id="4de9e-108">Shapes können ausgedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="4de9e-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="4de9e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4de9e-109">FALSE</span></span>  <br/> |<span data-ttu-id="4de9e-110">Shapes können nicht ausgedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="4de9e-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4de9e-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4de9e-111">Remarks</span></span>

<span data-ttu-id="4de9e-112">Sie können diesen Wert auch über die Option **Drucken** im Dialogfeld **Layereigenschaften** festlegen. (Klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**.)</span><span class="sxs-lookup"><span data-stu-id="4de9e-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="4de9e-113">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Print anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="4de9e-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4de9e-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4de9e-114">Cell name:</span></span>  <br/> |<span data-ttu-id="4de9e-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4de9e-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4de9e-116">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Print nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="4de9e-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4de9e-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4de9e-117">Section index:</span></span>  <br/> |<span data-ttu-id="4de9e-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="4de9e-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="4de9e-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4de9e-119">Row index:</span></span>  <br/> |<span data-ttu-id="4de9e-120">**visRowLayer**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4de9e-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4de9e-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4de9e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="4de9e-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="4de9e-122">**visDocPreviewScope**</span></span> <br/> |
   

