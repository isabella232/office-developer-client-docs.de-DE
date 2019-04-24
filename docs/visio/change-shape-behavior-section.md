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
# <a name="change-shape-behavior-section"></a>Abschnitt "Shape-Verhalten ändern"

Bestimmt die Eigenschaften, die während eines Ersetzungsvorgangs von der alten Form auf die Ersatzform übertragen werden. Die Werte der Zellen im Abschnitt **Shape-Verhalten ändern** des Master-Shapes der Ersetzung werden während der Form Ersetzung gelesen. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie die Zellen im Abschnitt **Shape-Verhalten ändern** festlegen, können Sie sicherstellen, dass bestimmte Eigenschaften des Ersatz-Shapes während des Ersetzungsvorgangs unverändert bleiben. Nicht geschützte Eigenschaften werden während des Vorgangs mit den lokalen Shape-Werten aus der alten Form aktualisiert. 
  
Sie können die Einstellungen für das Ersetzungs Verhalten eines Master-Shapes ändern, indem Sie das Master-Shape bearbeiten (Klicken Sie im Fenster **Shapes** mit der rechten Maustaste auf das Shape, zeigen Sie auf **Master bearbeiten**, und klicken Sie dann auf **Master-Shape bearbeiten**), und ändern Sie die Werte [der ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md)-, [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md)-, [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)-und [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) -Zellen im ShapeSheet des Masters. 
  
> [!NOTE]
> Sie können das Verhalten der Form Ersetzung der Shapes, die in den integrierten Schablonen in Microsoft Visio 2013 enthalten sind, nicht ändern. Um das Verhalten der Form Ersetzung der integrierten Visio-Shapes zu ändern, erstellen Sie eine neue Schablone, und fügen Sie die zu ändernde Form der neuen Schablone hinzu. 
  

