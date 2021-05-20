---
title: Zelle "ShapePermeablePlace" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Legt fest, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes unter Verwendung des Dialogfelds Layout konfigurieren (klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie anschließend auf Weitere Layoutoptionen) ausgerichtet werden.
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427220"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="24d0b-103">Zelle "ShapePermeablePlace" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="24d0b-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="24d0b-104">Legt fest, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes unter Verwendung des Dialogfelds **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie anschließend auf **Weitere Layoutoptionen**) ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="24d0b-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="24d0b-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="24d0b-105">**Value**</span></span>|<span data-ttu-id="24d0b-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="24d0b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="24d0b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="24d0b-107">TRUE</span></span>  <br/> |<span data-ttu-id="24d0b-108">Shapes können über einem Shape platziert werden.</span><span class="sxs-lookup"><span data-stu-id="24d0b-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="24d0b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="24d0b-109">FALSE</span></span>  <br/> |<span data-ttu-id="24d0b-110">Shapes können nicht über einem Shape platziert werden.</span><span class="sxs-lookup"><span data-stu-id="24d0b-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="24d0b-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="24d0b-111">Remarks</span></span>

<span data-ttu-id="24d0b-112">Sie können den Wert dieser Zelle auch auf der Registerkarte Platzierung im Dialogfeld [](run-in-developer-mode-display-the-developer-tab.md) Verhalten festlegen (wenn eine Form ausgewählt ist, klicken  Sie auf der Registerkarte Entwickler in der Gruppe **Shape-Entwurf** auf **Verhalten,** und klicken Sie dann auf die Registerkarte Platzierung).  </span><span class="sxs-lookup"><span data-stu-id="24d0b-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="24d0b-113">In Versionen vor Microsoft Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.</span><span class="sxs-lookup"><span data-stu-id="24d0b-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="24d0b-114">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ShapePermeablePlace anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="24d0b-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24d0b-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="24d0b-115">Cell name:</span></span>  <br/> |<span data-ttu-id="24d0b-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="24d0b-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="24d0b-117">Um einen Verweis auf die Zelle ShapePermeablePlace nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="24d0b-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="24d0b-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="24d0b-118">Section index:</span></span>  <br/> |<span data-ttu-id="24d0b-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="24d0b-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="24d0b-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="24d0b-120">Row index:</span></span>  <br/> |<span data-ttu-id="24d0b-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="24d0b-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="24d0b-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="24d0b-122">Cell index:</span></span>  <br/> |<span data-ttu-id="24d0b-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="24d0b-123">**visSLOPermeablePlace**</span></span> <br/> |
   

