---
title: Zelle "ReplaceCopyCells" (Abschnitt "Shape-Verhalten ändern")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Gibt eine Liste der Zellen im ShapeSheet an, die während einer Form Ersetzung aus einem alten Shape in die Ersatzform kopiert werden.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409342"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>Zelle "ReplaceCopyCells" (Abschnitt "Shape-Verhalten ändern")

Gibt eine Liste der Zellen im ShapeSheet an, die während einer Form Ersetzung aus einem alten Shape in die Ersatzform kopiert werden. 
  
## <a name="remarks"></a>Bemerkungen

Die Master-Form der Ersetzung muss einen **DependsOn** -Funktionsaufruf in der **ReplaceCopyCells** -Zelle enthalten, wobei jedes Argument in der Funktion ein Verweis auf eine Zelle ist. Diese Zellen werden von der alten Form in die Form kopiert, die aus einem Shape-Ersetzungsvorgang resultiert, unabhängig davon, wo Sie sich im ShapeSheet befinden. 
  
Werte und/oder Formeln, die auf andere Zellen verweisen, werden in die resultierende Form kopiert. Wenn die resultierende Form nicht über die Zelle referenziert wird, enthält die kopierte Zelle nur den Wert. 
  
Verweise in der **ReplaceCopyCells** Zellen Außerkraftsetzung für Zellen wie im Abschnitt **Protection** und die Zellen **ReplaceLockFormat**, **ReplaceLockShapeData**und **ReplaceLockText** definiert. 
  
Wenn Sie einen Verweis auf die Zelle **ReplaceCopyCells** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceCopyCells  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ReplaceCopyCells** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceCopyCells** <br/> |
   

