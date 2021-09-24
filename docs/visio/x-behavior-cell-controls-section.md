---
title: Zelle "X Behavior" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251285
ms.localizationpriority: medium
ms.assetid: 82423d08-b6ce-0f23-8b61-354c3e5f323e
description: Steuert die Art des Verhaltens, das die X-Koordinate des Steuerpunkts nach dem Verschieben des Ziehpunkts zeigt.
ms.openlocfilehash: f9dcb76c9ad8dcea5ace2580e41daae83dd27a10
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549315"
---
# <a name="x-behavior-cell-controls-section"></a>Zelle "X Behavior" (Abschnitt "Controls")

Steuert die Art  des Verhaltens, das die X-Koordinate des Steuerpunkts nach dem Verschieben des Ziehpunkts zeigt. 
  
|**Wert**|**Verhalten**|**Definition**|**Automatisierungskonstante**|
|:-----|:-----|:-----|:-----|
| 0  <br/> | Proportional  <br/> | Der Steuerpunkt kann verschoben werden, und seine Proportionen passen sich beim Dehnen eines Shapes diesem an.  <br/> |**visCtlProportional** <br/> |
| 1  <br/> | Proportional gesperrt  <br/> | Der Steuerpunkt wird proportional zum Shape verschoben, doch der Steuerpunkt selbst kann nicht verschoben werden.  <br/> |**visCtlLocked** <br/> |
| 2  <br/> | Abstand vom linken Rand  <br/> | Der Steuerpunkt befindet sich in einem konstanten Abstand zur linken Seite des Shapes.  <br/> |**visCtlOffsetMin** <br/> |
| 3  <br/> | Abstand von der Mitte  <br/> | Der Steuerpunkt befindet sich in einem konstanten Abstand zur Mitte des Shape.  <br/> |**visCtlOffsetMid** <br/> |
| 4   <br/> | Abstand vom rechten Rand  <br/> | Der Steuerpunkt befindet sich in einem konstanten Abstand zur rechten Seite des Shapes.  <br/> |**visCtlOffsetMax** <br/> |
| 5  <br/> | Proportional, verborgen  <br/> | Gleich 0, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlProportionalHidden** <br/> |
| 6   <br/> | Proportional gesperrt, verborgen  <br/> | Gleich 1, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlLockedHiddenv** <br/> |
| 7   <br/> | Abstand vom linken Rand, verborgen  <br/> | Gleich 2, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlOffsetMinHidden** <br/> |
| 8   <br/> | Abstand von der Mitte, verborgen  <br/> | Gleich 3, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlOffsetMidHidden** <br/> |
| 9   <br/> | Abstand vom rechten Rand, verborgen  <br/> | Gleich 4, jedoch ist der Steuerpunkt nicht sichtbar.  <br/> |**visCtlOffsetMaxHidden** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle X Behavior anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Steuerelemente.  *Name*  . XConwhere-Steuerelemente.  *Name*  ist der Name der Steuerelementzeile.  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle X Behavior anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionControls** <br/> |
| Zeilenindex:  <br/> |**visRowControl**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCtlXCon** <br/> |
   

