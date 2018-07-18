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
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798018"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="73cdf-103">ShapePermeablePlace Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="73cdf-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="73cdf-104">Legt fest, ob platzierbare Shapes über einem Shape platziert werden können, wenn Shapes unter Verwendung des Dialogfelds **Layout konfigurieren** (klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie anschließend auf **Weitere Layoutoptionen**) ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="73cdf-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="73cdf-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="73cdf-105">**Value**</span></span>|<span data-ttu-id="73cdf-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73cdf-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73cdf-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="73cdf-107">TRUE</span></span>  <br/> |<span data-ttu-id="73cdf-108">Shapes können über einem Shape platziert werden.</span><span class="sxs-lookup"><span data-stu-id="73cdf-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="73cdf-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="73cdf-109">FALSE</span></span>  <br/> |<span data-ttu-id="73cdf-110">Shapes können nicht über einem Shape platziert werden.</span><span class="sxs-lookup"><span data-stu-id="73cdf-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73cdf-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73cdf-111">Remarks</span></span>

<span data-ttu-id="73cdf-112">Sie können den Wert dieser Zelle auch festlegen, auf der Registerkarte **Platzierung** im Dialogfeld **Verhalten** (mit einem Shape ausgewählt haben, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** klicken Sie auf **das Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ).</span><span class="sxs-lookup"><span data-stu-id="73cdf-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="73cdf-113">In Versionen vor Visio  2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.</span><span class="sxs-lookup"><span data-stu-id="73cdf-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="73cdf-114">Wenn Sie einen Verweis auf die Zelle ShapePermeablePlace aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="73cdf-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73cdf-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="73cdf-115">Cell name:</span></span>  <br/> |<span data-ttu-id="73cdf-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="73cdf-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="73cdf-117">Wenn Sie einen Verweis auf die Zelle ShapePermeablePlace aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="73cdf-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="73cdf-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="73cdf-118">Section index:</span></span>  <br/> |<span data-ttu-id="73cdf-119">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="73cdf-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="73cdf-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="73cdf-120">Row index:</span></span>  <br/> |<span data-ttu-id="73cdf-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="73cdf-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="73cdf-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="73cdf-122">Cell index:</span></span>  <br/> |<span data-ttu-id="73cdf-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="73cdf-123">**visSLOPermeablePlace**</span></span> <br/> |
   

