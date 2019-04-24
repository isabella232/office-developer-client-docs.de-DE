---
title: Zelle "ShapePermeableX" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: Legt fest, ob ein Verbinder horizontal durch ein platzierbares Shape geleitet werden kann.
ms.openlocfilehash: 21fa1683c4b1afd24992ec7a8a6daa52a8280825
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357050"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a><span data-ttu-id="9e121-103">Zelle "ShapePermeableX" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="9e121-103">ShapePermeableX Cell (Shape Layout Section)</span></span>

<span data-ttu-id="9e121-104">Legt fest, ob ein Verbinder horizontal durch ein platzierbares Shape geleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9e121-104">Determines whether a connector can route horizontally through a placeable shape.</span></span>
  
|<span data-ttu-id="9e121-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9e121-105">**Value**</span></span>|<span data-ttu-id="9e121-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e121-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9e121-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9e121-107">TRUE</span></span>  <br/> |<span data-ttu-id="9e121-108">Verbinder können horizontal durch ein platzierbares Shape geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9e121-108">Enable connectors to route horizontally through a placeable shape.</span></span>  <br/> |
|<span data-ttu-id="9e121-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9e121-109">FALSE</span></span>  <br/> |<span data-ttu-id="9e121-110">Verbinder können nicht horizontal durch ein platzierbares Shape geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="9e121-110">Do not let connectors route horizontally through a placeable shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9e121-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e121-111">Remarks</span></span>

<span data-ttu-id="9e121-112">Sie können den Wert dieser Zelle auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (wenn ein Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ).</span><span class="sxs-lookup"><span data-stu-id="9e121-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="9e121-113">In Versionen vor Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9e121-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="9e121-114">Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeableX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9e121-114">To get a reference to the ShapePermeableX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e121-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9e121-115">Cell name:</span></span>  <br/> |<span data-ttu-id="9e121-116">Zelle ShapePermeableX</span><span class="sxs-lookup"><span data-stu-id="9e121-116">ShapePermeableX</span></span>  <br/> |
   
<span data-ttu-id="9e121-117">Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeableX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9e121-117">To get a reference to the ShapePermeableX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9e121-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9e121-118">Section index:</span></span>  <br/> |<span data-ttu-id="9e121-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9e121-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9e121-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9e121-120">Row index:</span></span>  <br/> |<span data-ttu-id="9e121-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="9e121-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="9e121-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9e121-122">Cell index:</span></span>  <br/> |<span data-ttu-id="9e121-123">**visSLOPermX**</span><span class="sxs-lookup"><span data-stu-id="9e121-123">**visSLOPermX**</span></span> <br/> |
   

