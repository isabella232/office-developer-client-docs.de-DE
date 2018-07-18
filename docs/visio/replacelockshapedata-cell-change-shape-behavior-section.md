---
title: ReplaceLockShapeData Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben. Die ReplaceLockShapeData bestimmt, ob die Shape-Daten des master-Shapes überschreibt alle Shape-Daten der Form ersetzt werden.
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797847"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>ReplaceLockShapeData Cell (Change Shape Behavior Section)

Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben. Die **ReplaceLockShapeData** bestimmt, ob die Shape-Daten des master-Shapes aller der Form ersetzt die Shape-Daten überschreibt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1 (WAHR)  <br/> |Alle Zeilen und Werte des **Shape** -Datenabschnitt des master-Shapes auf das Ersatz-Shape kopiert wurden, und alle lokalen Werte vom alten Shape ersetzt werden verworfen.  <br/> |
|0 (FALSE)  <br/> |Die Zeilen und Werte der **Shape** -Datenabschnitt des master-Shapes werden zum Ersatz-Shape kopiert. Alle Zeilen in der **Shape** -Datenabschnitt der alten Form mit lokalen Werte werden zum Ersatz-Shape übertragen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **ReplaceLockShapeData** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockShapeData  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ReplaceLockShapeData** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockShapeData** <br/> |
   

