---
title: Zelle "ReplaceLockShapeData" (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shape-Ersetzungsvorgangs ersetzt wird. ReplaceLockShapeData bestimmt, ob die Shape-Daten des Master-Shapes alle Shape-Daten des zu ersetzenden Shapes überschreiben.
ms.openlocfilehash: 98e6c5be4519a55f0207df53dc169604c0718cb4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627646"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>Zelle "ReplaceLockShapeData" (Abschnitt "Change Shape Behavior")

Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shape-Ersetzungsvorgangs ersetzt wird. **ReplaceLockShapeData** bestimmt, ob die Shape-Daten des Master-Shapes alle Shape-Daten des zu ersetzenden Shapes überschreiben. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1 (TRUE)  <br/> |Alle Zeilen und Werte des **Shape-Datenabschnitts** des Master-Shapes werden in das Ersatz-Shape kopiert, und alle lokalen Werte aus dem alten Shape, das ersetzt wird, werden verworfen.  <br/> |
|0 (FALSE)  <br/> |Die Zeilen und Werte des **Shape-Datenabschnitts** des Master-Shapes werden in das Ersatz-Shape kopiert. Alle Zeilen im **Abschnitt Shape-Daten** des alten Shapes mit lokalen Werten werden an das Ersatz-Shape übertragen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "ReplaceLockShapeData"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockShapeData  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **"ReplaceLockShapeData"** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockShapeData** <br/> |
   

