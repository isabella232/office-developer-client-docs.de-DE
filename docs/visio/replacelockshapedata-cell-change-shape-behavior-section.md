---
title: Zelle ReplaceLockShapeData (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird. ReplaceLockShapeData bestimmt, ob die Formdaten der Masterform alle Formdaten der ersetzten Form überschreiben.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408873"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>Zelle ReplaceLockShapeData (Abschnitt "Change Shape Behavior")

Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird. **ReplaceLockShapeData** bestimmt, ob die Formdaten der Masterform alle Formdaten der ersetzten Form überschreiben. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1 (TRUE)  <br/> |Alle Zeilen und Werte des Abschnitts **"Shape Data"** der Masterform werden in die Ersatzform kopiert, und alle lokalen Werte aus dem alten Shape, das ersetzt wird, werden verworfen.  <br/> |
|0 (FALSE)  <br/> |Die Zeilen und Werte des **Abschnitts Shape Data** des Master-Shapes werden in die Ersetzungsform kopiert. Alle Zeilen im **Abschnitt Shape Data** der alten Form mit lokalen Werten werden auf die Ersatzform übertragen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle ReplaceLockShapeData** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockShapeData  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ReplaceLockShapeData** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockShapeData** <br/> |
   

