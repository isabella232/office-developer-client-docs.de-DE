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
ms.openlocfilehash: 62f8bfa0fdfb5c483836f344e8b784dc9092fded
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417518"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a><span data-ttu-id="278de-103">Zelle "ShapePermeableY" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="278de-103">ShapePermeableY Cell (Shape Layout Section)</span></span>

<span data-ttu-id="278de-104">Legt fest, ob ein Verbinder vertikal durch ein Shape geleitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="278de-104">Determines whether a connector can route vertically through a shape.</span></span>
  
|<span data-ttu-id="278de-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="278de-105">**Value**</span></span>|<span data-ttu-id="278de-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="278de-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="278de-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="278de-107">TRUE</span></span>  <br/> |<span data-ttu-id="278de-108">Verbinder können vertikal durch ein Shape geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="278de-108">Enable connectors to route vertically through a shape.</span></span>  <br/> |
|<span data-ttu-id="278de-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="278de-109">FALSE</span></span>  <br/> |<span data-ttu-id="278de-110">Verbinder können nicht vertikal durch ein Shape geleitet werden.</span><span class="sxs-lookup"><span data-stu-id="278de-110">Do not let connectors route vertically through a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="278de-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="278de-111">Remarks</span></span>

<span data-ttu-id="278de-112">Sie können den Wert dieser Zelle auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (wenn ein Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ).</span><span class="sxs-lookup"><span data-stu-id="278de-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="278de-113">In Versionen vor Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.</span><span class="sxs-lookup"><span data-stu-id="278de-113">In versions earlier than Visio 2000, you set this behavior by using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="278de-114">Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeableY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="278de-114">To get a reference to the ShapePermeableY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="278de-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="278de-115">Cell name:</span></span>  <br/> |<span data-ttu-id="278de-116">Zelle ShapePermeableY</span><span class="sxs-lookup"><span data-stu-id="278de-116">ShapePermeableY</span></span>  <br/> |
   
<span data-ttu-id="278de-117">Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeableY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="278de-117">To get a reference to the ShapePermeableY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="278de-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="278de-118">Section index:</span></span>  <br/> |<span data-ttu-id="278de-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="278de-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="278de-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="278de-120">Row index:</span></span>  <br/> |<span data-ttu-id="278de-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="278de-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="278de-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="278de-122">Cell index:</span></span>  <br/> |<span data-ttu-id="278de-123">**visSLOPermY**</span><span class="sxs-lookup"><span data-stu-id="278de-123">**visSLOPermY**</span></span> <br/> |
   

