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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357057"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="29633-103">Zelle "ShapePermeablePlace" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="29633-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="29633-104">Legt fest, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes unter Verwendung des Dialogfelds **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie anschließend auf **Weitere Layoutoptionen**) ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="29633-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="29633-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="29633-105">**Value**</span></span>|<span data-ttu-id="29633-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="29633-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29633-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="29633-107">TRUE</span></span>  <br/> |<span data-ttu-id="29633-108">Shapes können über einem Shape platziert werden.</span><span class="sxs-lookup"><span data-stu-id="29633-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="29633-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="29633-109">FALSE</span></span>  <br/> |<span data-ttu-id="29633-110">Shapes können nicht über einem Shape platziert werden.</span><span class="sxs-lookup"><span data-stu-id="29633-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29633-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29633-111">Remarks</span></span>

<span data-ttu-id="29633-112">Sie können den Wert dieser Zelle auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (wenn ein Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ).</span><span class="sxs-lookup"><span data-stu-id="29633-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="29633-113">In Versionen vor Microsoft Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.</span><span class="sxs-lookup"><span data-stu-id="29633-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="29633-114">Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeablePlace aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="29633-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29633-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="29633-115">Cell name:</span></span>  <br/> |<span data-ttu-id="29633-116">Zelle ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="29633-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="29633-117">Wenn Sie einen Verweis auf die Zelle Zelle ShapePermeablePlace aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="29633-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="29633-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="29633-118">Section index:</span></span>  <br/> |<span data-ttu-id="29633-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="29633-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="29633-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="29633-120">Row index:</span></span>  <br/> |<span data-ttu-id="29633-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="29633-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="29633-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="29633-122">Cell index:</span></span>  <br/> |<span data-ttu-id="29633-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="29633-123">**visSLOPermeablePlace**</span></span> <br/> |
   

