---
title: Zelle "X Behavior" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251285
localization_priority: Normal
ms.assetid: 82423d08-b6ce-0f23-8b61-354c3e5f323e
description: Steuert die Art des Verhaltens, das die x-Koordinate des Steuerpunkts zeigt, nachdem der Ziehpunkt verschoben wurde.
ms.openlocfilehash: 50b08664deec69659ff70a0bf9a17a148ed0e110
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338843"
---
# <a name="x-behavior-cell-controls-section"></a>Zelle "X Behavior" (Abschnitt "Controls")

Steuert die Art des Verhaltens, das die *x* -Koordinate des Steuerpunkts zeigt, nachdem der Ziehpunkt verschoben wurde. 
  
|**Wert**|**Verhalten**|**Definition**|**Automatisierungskonstante**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | Proportional  <br/> | Der Steuerpunkt kann verschoben werden, und seine Proportionen passen sich beim Dehnen eines Shapes diesem an.  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | Proportional gesperrt  <br/> | Der Steuerpunkt wird proportional zum Shape verschoben, doch der Steuerpunkt selbst kann nicht verschoben werden.  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | Abstand vom linken Rand  <br/> | Der Steuerpunkt befindet sich in einem konstanten Abstand zur linken Seite des Shapes.  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | Abstand von der Mitte  <br/> | Der Steuerpunkt befindet sich in einem konstanten Abstand zur Mitte des Shape.  <br/> |**visCtlOffsetMid** <br/> |
| 4  <br/> | Abstand vom rechten Rand  <br/> | Der Steuerpunkt befindet sich in einem konstanten Abstand zur rechten Seite des Shapes.  <br/> |**visCtlOffsetMax** <br/> |
| 5  <br/> | Proportional, verborgen  <br/> | Gleich 0, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlProportionalHidden** <br/> |
| 6  <br/> | Proportional gesperrt, verborgen  <br/> | Gleich 1, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlLockedHiddenv** <br/> |
| 7  <br/> | Abstand vom linken Rand, verborgen  <br/> | Gleich 2, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8  <br/> | Abstand von der Mitte, verborgen  <br/> | Gleich 3, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9  <br/> | Abstand vom rechten Rand, verborgen  <br/> | Gleich 4, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle X Behavior aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name* . XConwhere-Steuerelemente.  *Name* ist der Name der Zeile Controls.  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X Behavior aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlXCon** <br/> |
   

