---
title: Abschnitt "Shape-Verhalten ändern"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Bestimmt die Eigenschaften, die während eines Ersetzungsvorgangs von der alten Form auf die Ersatzform übertragen werden. Die Werte der Zellen im Abschnitt Shape-Verhalten ändern des Master-Shapes der Ersetzung werden während der Form Ersetzung gelesen.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341923"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="b3fed-104">Abschnitt "Shape-Verhalten ändern"</span><span class="sxs-lookup"><span data-stu-id="b3fed-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="b3fed-105">Bestimmt die Eigenschaften, die während eines Ersetzungsvorgangs von der alten Form auf die Ersatzform übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="b3fed-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="b3fed-106">Die Werte der Zellen im Abschnitt **Shape-Verhalten ändern** des Master-Shapes der Ersetzung werden während der Form Ersetzung gelesen.</span><span class="sxs-lookup"><span data-stu-id="b3fed-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b3fed-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3fed-107">Remarks</span></span>

<span data-ttu-id="b3fed-108">Wenn Sie die Zellen im Abschnitt **Shape-Verhalten ändern** festlegen, können Sie sicherstellen, dass bestimmte Eigenschaften des Ersatz-Shapes während des Ersetzungsvorgangs unverändert bleiben.</span><span class="sxs-lookup"><span data-stu-id="b3fed-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="b3fed-109">Nicht geschützte Eigenschaften werden während des Vorgangs mit den lokalen Shape-Werten aus der alten Form aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="b3fed-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="b3fed-110">Sie können die Einstellungen für das Ersetzungs Verhalten eines Master-Shapes ändern, indem Sie das Master-Shape bearbeiten (Klicken Sie im Fenster **Shapes** mit der rechten Maustaste auf das Shape, zeigen Sie auf **Master bearbeiten**, und klicken Sie dann auf **Master-Shape bearbeiten**), und ändern Sie die Werte [der ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md)-, [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md)-, [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)-und [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) -Zellen im ShapeSheet des Masters.</span><span class="sxs-lookup"><span data-stu-id="b3fed-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="b3fed-111">Sie können das Verhalten der Form Ersetzung der Shapes, die in den integrierten Schablonen in Microsoft Visio 2013 enthalten sind, nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="b3fed-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="b3fed-112">Um das Verhalten der Form Ersetzung der integrierten Visio-Shapes zu ändern, erstellen Sie eine neue Schablone, und fügen Sie die zu ändernde Form der neuen Schablone hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3fed-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

