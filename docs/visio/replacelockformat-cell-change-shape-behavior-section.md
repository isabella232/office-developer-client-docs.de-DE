---
title: Zelle ReplaceLockFormat (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird. Wenn die Zelle ReplaceLockFormat eines Master-Shapes auf TRUE (1) festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das durch den Master ersetzt wird.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427234"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>Zelle ReplaceLockFormat (Abschnitt "Change Shape Behavior")

Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird. Wenn die **Zelle ReplaceLockFormat** eines Master-Shapes auf TRUE (1) festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das durch den Master ersetzt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Wenn die **Zelle ReplaceLockFormat** eines Master-Shapes auf TRUE festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das durch den Master ersetzt wird.  <br/> |
|FALSE  <br/> |Wenn die **Zelle ReplaceLockFormat** eines Master-Shapes auf FALSE festgelegt ist, enthält die Ersatzform die lokalen Formatierungswerte aus der alten Form nach dem Ersetzungsvorgang.  <br/> |
   
## <a name="remarks"></a>Hinweise

Die **Zelle ReplaceLockFormat** bestimmt, ob die Masterform die lokalen Formatierungswerte der Zellen in den folgenden Abschnitten während eines Shapeersetzungsvorgangs überschreibt: 
  
- **Abschnitt "Fill Format"** 
    
- **Abschnitt "Linienformat"** 
    
- **Abschnitt "Quick Style"** 
    
- **Abschnitt "Designeigenschaften"** 
    
- **Abschnitt "Gradient Properties"** 
    
- **Abschnitt "Abschrägungseigenschaften"** 
    
- **Abschnitt "Zusätzliche Effekteigenschaften"** 
    
- **Abschnitt "Line Gradient Stops"** 
    
- **Abschnitt "Füllgradientenstopps"** 
    
Um einen Verweis auf die **Zelle ReplaceLockFormat** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockFormat  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ReplaceLockFormat** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockFormat** <br/> |
   

