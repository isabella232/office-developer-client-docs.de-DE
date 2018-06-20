---
title: Zelle "ShapePermeableY" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: Legt fest, ob ein Verbinder vertikal durch ein Shape geleitet werden kann.
ms.openlocfilehash: 4a7a389ec1d753b8582b7ff0b921a615e582b1ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798015"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a><span data-ttu-id="c4490-103">ShapePermeableY Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="c4490-103">ShapePermeableY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="c4490-104">Legt fest, ob ein Verbinder vertikal durch ein Shape geleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4490-104">Determines whether a connector can route vertically through a shape.</span></span>
  
|<span data-ttu-id="c4490-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c4490-105">**Value**</span></span>|<span data-ttu-id="c4490-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c4490-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c4490-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c4490-107">TRUE</span></span>  <br/> |<span data-ttu-id="c4490-108">Verbinder können vertikal durch ein Shape geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c4490-108">Enable connectors to route vertically through a shape.</span></span>  <br/> |
|<span data-ttu-id="c4490-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c4490-109">FALSE</span></span>  <br/> |<span data-ttu-id="c4490-110">Verbinder können nicht vertikal durch ein Shape geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="c4490-110">Do not let connectors route vertically through a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c4490-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4490-111">Remarks</span></span>

<span data-ttu-id="c4490-112">Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** (mit einem Shape ausgewählt haben, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** klicken Sie auf **das Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ).</span><span class="sxs-lookup"><span data-stu-id="c4490-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="c4490-113">In Versionen vor Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c4490-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="c4490-114">Wenn Sie einen Verweis auf die Zelle ShapePermeableY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c4490-114">To get a reference to the ShapePermeableY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4490-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c4490-115">Cell name:</span></span>  <br/> |<span data-ttu-id="c4490-116">ShapePermeableY</span><span class="sxs-lookup"><span data-stu-id="c4490-116">ShapePermeableY</span></span>  <br/> |
   
<span data-ttu-id="c4490-117">Wenn Sie einen Verweis auf die Zelle ShapePermeableY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c4490-117">To get a reference to the ShapePermeableY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c4490-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c4490-118">Section index:</span></span>  <br/> |<span data-ttu-id="c4490-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c4490-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c4490-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c4490-120">Row index:</span></span>  <br/> |<span data-ttu-id="c4490-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="c4490-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="c4490-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c4490-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c4490-123">**visSLOPermY**</span><span class="sxs-lookup"><span data-stu-id="c4490-123">**visSLOPermY**</span></span> <br/> |
   

