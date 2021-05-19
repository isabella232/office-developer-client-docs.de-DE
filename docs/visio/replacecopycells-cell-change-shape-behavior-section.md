---
title: Zelle "ReplaceCopyCells" (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Gibt eine Liste der Zellen im ShapeSheet an, die während eines Shapeersetzungsvorgangs von einer alten Form in die Ersatzform kopiert werden.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409342"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>Zelle "ReplaceCopyCells" (Abschnitt "Change Shape Behavior")

Gibt eine Liste der Zellen im ShapeSheet an, die während eines Shapeersetzungsvorgangs von einer alten Form in die Ersatzform kopiert werden. 
  
## <a name="remarks"></a>Hinweise

Die Masterform der Ersetzung muss einen **DEPENDSON-Funktionsaufruf** in der **Zelle ReplaceCopyCells** enthalten, wobei jedes Argument in der Funktion ein Verweis auf eine Zelle ist. Diese Zellen werden aus der alten Form in die Form kopiert, die aus einem Shape-Ersetzungsvorgang resultiert, unabhängig davon, wo sie sich im ShapeSheet befinden. 
  
Werte und/oder Formeln, die auf andere Zellen verweisen, werden in die resultierende Form kopiert. Wenn die resultierende Form nicht über die referenzierte Zelle verfügt, enthält die kopierte Zelle nur den Wert. 
  
Verweise im **ReplaceCopyCells-Zellüberschreibungsschutzsatz** für Zellen, wie im Abschnitt **Protection** definiert, und die **Zellen ReplaceLockFormat,** **ReplaceLockShapeData** und **ReplaceLockText.** 
  
Um einen Verweis auf die **Zelle ReplaceCopyCells anhand** des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceCopyCells  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ReplaceCopyCells** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceCopyCells** <br/> |
   

