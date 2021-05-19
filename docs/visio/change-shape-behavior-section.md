---
title: Abschnitt "Shape-Verhalten ändern"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Bestimmt die Eigenschaften, die während eines Ersetzungsvorgangs von der alten Form auf die Ersatzform übertragen werden. Die Werte der Zellen im Abschnitt ShapeVerhalten ändern des Master-Shapes der Ersetzung werden während des Shapeersetzungsvorgangs gelesen.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418666"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="9a3ee-104">Abschnitt "Shape-Verhalten ändern"</span><span class="sxs-lookup"><span data-stu-id="9a3ee-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="9a3ee-105">Bestimmt die Eigenschaften, die während eines Ersetzungsvorgangs von der alten Form auf die Ersatzform übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="9a3ee-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="9a3ee-106">Die Werte der Zellen im Abschnitt **ShapeVerhalten** ändern des Master-Shapes der Ersetzung werden während des Shapeersetzungsvorgangs gelesen.</span><span class="sxs-lookup"><span data-stu-id="9a3ee-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="9a3ee-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9a3ee-107">Remarks</span></span>

<span data-ttu-id="9a3ee-108">Durch Festlegen der Zellen im Abschnitt **Shapeverhalten** ändern können Sie sicherstellen, dass bestimmte Eigenschaften der Ersatzform während des Ersetzungsvorgangs unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="9a3ee-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="9a3ee-109">Eigenschaften, die nicht geschützt sind, werden während des Vorgangs mit den lokalen Shapewerten der alten Form aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="9a3ee-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="9a3ee-110">Sie können die Einstellungen für das Ersetzungsverhalten eines Master-Shapes ändern, indem Sie die Master-Form bearbeiten (klicken Sie im **Fenster Shapes** mit der rechten Maustaste auf die Form, zeigen Sie auf Master **bearbeiten,** und klicken Sie dann auf **Master-Shape** bearbeiten) und die Werte der Zellen [ReplaceCopyCells,](replacecopycells-cell-change-shape-behavior-section.md) [ReplaceLockFormat,](replacelockformat-cell-change-shape-behavior-section.md) [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)und [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) im ShapeSheet des Masters ändern.</span><span class="sxs-lookup"><span data-stu-id="9a3ee-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9a3ee-111">Sie können das Verhalten des Shapeersetzungsverhaltens der Shapes, die in den integrierten Schablonen in Microsoft Visio 2013 enthalten sind, nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="9a3ee-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="9a3ee-112">Erstellen Sie eine neue Schablone, und fügen Sie der neuen Schablone die Form hinzu, die Sie ändern möchten, um das Verhalten des Formersetzungsverhaltens der integrierten Visio-Shapes zu ändern.</span><span class="sxs-lookup"><span data-stu-id="9a3ee-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

