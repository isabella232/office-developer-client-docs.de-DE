---
title: Zelle "ReplaceLockShapeData" (Abschnitt "Shape-Verhalten ändern")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird. Die ReplaceLockShapeData bestimmt, ob die Shape-Daten des Master-Shapes alle Shape-Daten der Form überschreiben, die ersetzt wird.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348342"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a>Zelle "ReplaceLockShapeData" (Abschnitt "Shape-Verhalten ändern")

Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird. Die **ReplaceLockShapeData** bestimmt, ob die Shape-Daten des Master-Shapes alle Shape-Daten der Form überschreiben, die ersetzt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|1 (TRUE)  <br/> |Alle Zeilen und Werte des **Shape-Daten** Abschnitts des Master-Shapes werden in das Ersatz-Shape kopiert, und alle lokalen Werte aus dem alten zu ersetzenden Shape werden verworfen.  <br/> |
|0 (FALSCH)  <br/> |Die Zeilen und Werte des **Shape-Daten** Abschnitts des Master-Shapes werden in die Ersatzform kopiert. Alle Zeilen im **Shape-Daten** Abschnitt des alten Shapes mit lokalen Werten werden an das Ersatz-Shape übertragen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **ReplaceLockShapeData** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockShapeData  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ReplaceLockShapeData** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockShapeData** <br/> |
   

