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
# <a name="change-shape-behavior-section"></a>Abschnitt "Shape-Verhalten ändern"

Bestimmt die Eigenschaften, die während eines Ersetzungsvorgangs von der alten Form auf die Ersatzform übertragen werden. Die Werte der Zellen im Abschnitt **ShapeVerhalten** ändern des Master-Shapes der Ersetzung werden während des Shapeersetzungsvorgangs gelesen. 
  
## <a name="remarks"></a>Hinweise

Durch Festlegen der Zellen im Abschnitt **Shapeverhalten** ändern können Sie sicherstellen, dass bestimmte Eigenschaften der Ersatzform während des Ersetzungsvorgangs unverändert bleiben. Eigenschaften, die nicht geschützt sind, werden während des Vorgangs mit den lokalen Shapewerten der alten Form aktualisiert. 
  
Sie können die Einstellungen für das Ersetzungsverhalten eines Master-Shapes ändern, indem Sie die Master-Form bearbeiten (klicken Sie im **Fenster Shapes** mit der rechten Maustaste auf die Form, zeigen Sie auf Master **bearbeiten,** und klicken Sie dann auf **Master-Shape** bearbeiten) und die Werte der Zellen [ReplaceCopyCells,](replacecopycells-cell-change-shape-behavior-section.md) [ReplaceLockFormat,](replacelockformat-cell-change-shape-behavior-section.md) [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)und [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) im ShapeSheet des Masters ändern. 
  
> [!NOTE]
> Sie können das Verhalten des Shapeersetzungsverhaltens der Shapes, die in den integrierten Schablonen in Microsoft Visio 2013 enthalten sind, nicht ändern. Erstellen Sie eine neue Schablone, und fügen Sie der neuen Schablone die Form hinzu, die Sie ändern möchten, um das Verhalten des Formersetzungsverhaltens der integrierten Visio-Shapes zu ändern. 
  

