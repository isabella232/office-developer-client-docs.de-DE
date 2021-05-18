---
title: Zelle "Y Behavior" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1190
localization_priority: Normal
ms.assetid: 6d5062d3-743b-8664-8ec9-5a8f11d5edf9
description: Steuert die Art des Verhaltens, das die y-Koordinate des Steuerelementhandles nach dem Verschoben des Handles zeigt. Diese Formeln stehen zur Verfügung.
ms.openlocfilehash: bf8cbd490884244c92b68784dcbf041093539c94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413577"
---
# <a name="y-behavior-cell-controls-section"></a>Zelle "Y Behavior" (Abschnitt "Controls")

Steuert die Art des Verhaltens, das die y-Koordinate des Steuerelementhandles nach dem Verschoben des Handles zeigt.  Diese Formeln stehen zur Verfügung. 
  
|**Wert**|**Verhalten**|**Definition**|**Automatisierungskonstante**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | Proportional  <br/> | Der Steuerpunkt kann verschoben werden, und seine Proportionen passen sich beim Dehnen eines Shapes diesem an.  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | Proportional gesperrt  <br/> | Der Steuerpunkt wird proportional zum Shape verschoben, doch der Steuerpunkt selbst kann nicht verschoben werden.  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | Abstand vom unteren Rand  <br/> | Der Steuerpunkt befindet sich in einem konstanten Abstand zum unteren Rand des Shapes.  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | Abstand von der Mitte  <br/> | Der Steuerpunkt befindet sich in einem konstanten Abstand zur Mitte des Shape.  <br/> |**visCtlOffsetMid** <br/> |
| 4   <br/> | Abstand vom oberen Rand  <br/> | Der Steuerpunkt befindet sich in einem konstanten Abstand zum oberen Rand des Shapes.  <br/> |**visCtlOffsetMax** <br/> |
| 5   <br/> | Proportional, verborgen  <br/> | Gleich 0, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlProportionalHidden** <br/> |
| 6   <br/> | Proportional gesperrt, verborgen  <br/> | Gleich 1, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlLockedHiddenv** <br/> |
| 7   <br/> | Abstand vom linken Rand, verborgen  <br/> | Gleich 2, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8   <br/> | Abstand von der Mitte, verborgen  <br/> | Gleich 3, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9   <br/> | Abstand vom rechten Rand, verborgen  <br/> | Gleich 4, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle "Y Behavior" anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name*  . YConwhere-Steuerelemente.  *name*  ist der Name der Steuerelementzeile.  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "Y Behavior" nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlYCon** <br/> |
   

