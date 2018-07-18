---
title: ReplaceCopyCells Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Gibt eine Liste der Zellen im ShapeSheet, die während ein Shape Ersetzungsvorgang aus einer alten Form zum Ersatz-Shape kopiert werden.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797812"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a>ReplaceCopyCells Cell (Change Shape Behavior Section)

Gibt eine Liste der Zellen im ShapeSheet, die während ein Shape Ersetzungsvorgang aus einer alten Form zum Ersatz-Shape kopiert werden. 
  
## <a name="remarks"></a>Bemerkungen

Das master-Shape die Ersetzung muss einen Funktionsaufruf **DEPENDSON** in der Zelle **ReplaceCopyCells** enthalten, wobei jedes Argument in der Funktion einen Verweis auf eine Zelle ist. Betroffenen Zellen werden von der alten Form mit dem Shape kopiert, die eine Form Ersetzungsoperation, unabhängig davon, wo sie sich im ShapeSheet sind ergibt. 
  
Werte und/oder Formeln, die von anderen Zellen referenziert werden im resultierenden Shape kopiert. Wenn das resultierende Shape die referenzierte Zelle nicht vorhanden ist, enthält die kopierte Zelle nur den Wert. 
  
Verweise in der Zelle **ReplaceCopyCells** außer Kraft setzen Schutz auf Zellen gemäß Definition im Abschnitt " **Protection** " und die **ReplaceLockFormat**, **ReplaceLockShapeData**und **ReplaceLockText** Zellen festgelegt. 
  
Wenn Sie einen Verweis auf die Zelle **ReplaceCopyCells** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceCopyCells  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ReplaceCopyCells** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceCopyCells** <br/> |
   

