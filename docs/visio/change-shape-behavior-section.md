---
title: Abschnitt "Change Shape Behavior"
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Bestimmt die Eigenschaften, die während eines Ersetzungsvorgangs von der alten Form auf das Ersetzungs-Shape übertragen werden. Die Werte der Zellen im Abschnitt Shape-Verhalten ändern des Master-Shapes des Ersetzungsvorgangs werden während des Vorgangs zum Ersetzen der Form gelesen.
ms.openlocfilehash: 4bc87c7ab77568b06ced5456c74f96c151322761
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577997"
---
# <a name="change-shape-behavior-section"></a>Abschnitt "Change Shape Behavior"

Bestimmt die Eigenschaften, die während eines Ersetzungsvorgangs von der alten Form auf das Ersetzungs-Shape übertragen werden. Die Werte der Zellen im Abschnitt **Shape-Verhalten** ändern des Master-Shapes des Ersetzungsvorgangs werden während des Vorgangs zum Ersetzen der Form gelesen. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Durch Festlegen der Zellen im Abschnitt zum Ändern des **Shape-Verhaltens** können Sie sicherstellen, dass bestimmte Eigenschaften des Ersetzungs-Shapes während des Ersetzungsvorgangs unverändert bleiben. Eigenschaften, die nicht geschützt sind, werden während des Vorgangs mit den lokalen Shape-Werten aus dem alten Shape aktualisiert. 
  
Sie können die Einstellungen für das Ersetzungsverhalten eines  Master-Shapes ändern, indem Sie das Master-Shape bearbeiten (klicken Sie im Shape-Fenster mit der rechten Maustaste auf das Shape, zeigen Sie auf Master **bearbeiten,** und klicken Sie dann auf **Master-Shape bearbeiten),** und ändern Sie die Werte der Zellen [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)und [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) im ShapeSheet des Master-Shapes. 
  
> [!NOTE]
> Sie können das Verhalten beim Ersetzen von Shapes, die in den integrierten Schablonen in Microsoft Visio 2013 enthalten sind, nicht ändern. Um das Verhalten beim Ersetzen von Formen der integrierten Visio Shapes zu ändern, erstellen Sie eine neue Schablone, und fügen Sie der neuen Schablone das Shape hinzu, das Sie ändern möchten. 
  

