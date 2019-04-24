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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356182"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="7c280-103">Zelle "Print" (Abschnitt "Layers")</span><span class="sxs-lookup"><span data-stu-id="7c280-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="7c280-104">Gibt an, ob die dem Layer zugehörigen Shapes ausgedruckt werden können.</span><span class="sxs-lookup"><span data-stu-id="7c280-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="7c280-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7c280-105">**Value**</span></span>|<span data-ttu-id="7c280-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7c280-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7c280-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="7c280-107">TRUE</span></span>  <br/> |<span data-ttu-id="7c280-108">Shapes können ausgedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="7c280-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="7c280-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="7c280-109">FALSE</span></span>  <br/> |<span data-ttu-id="7c280-110">Shapes können nicht ausgedruckt werden.</span><span class="sxs-lookup"><span data-stu-id="7c280-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7c280-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7c280-111">Remarks</span></span>

<span data-ttu-id="7c280-112">Sie können diesen Wert auch über die Option **Drucken** im Dialogfeld **Layereigenschaften** festlegen. (Klicken Sie dazu auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **Layer**, und klicken Sie dann auf **Layereigenschaften**.)</span><span class="sxs-lookup"><span data-stu-id="7c280-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="7c280-113">Wenn Sie einen Verweis auf die Zelle "Print" aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7c280-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c280-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7c280-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7c280-115">Layers. print [ *i* ] wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7c280-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7c280-116">Wenn Sie einen Verweis auf die Zelle "Print" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7c280-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c280-117">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7c280-117">Section index:</span></span>  <br/> |<span data-ttu-id="7c280-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="7c280-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="7c280-119">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7c280-119">Row index:</span></span>  <br/> |<span data-ttu-id="7c280-120">**visRowLayer** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7c280-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7c280-121">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7c280-121">Cell index:</span></span>  <br/> |<span data-ttu-id="7c280-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="7c280-122">**visDocPreviewScope**</span></span> <br/> |
   

