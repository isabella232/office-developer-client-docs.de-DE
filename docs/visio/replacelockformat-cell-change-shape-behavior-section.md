---
title: Zelle "ReplaceLockFormat" (Abschnitt "Shape-Verhalten ändern")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird. Wenn die Zelle ReplaceLockFormat eines Master-Shapes auf TRUE (1) festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das vom Master ersetzt wird.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329890"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>Zelle "ReplaceLockFormat" (Abschnitt "Shape-Verhalten ändern")

Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird. Wenn die Zelle **ReplaceLockFormat** eines Master-Shapes auf true (1) festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das vom Master ersetzt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Wenn die Zelle **ReplaceLockFormat** eines Master-Shapes auf true festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das vom Master ersetzt wird.  <br/> |
|FALSE  <br/> |Wenn die Zelle **ReplaceLockFormat** eines Master-Shapes auf false festgelegt ist, enthält die Ersatzform die lokalen Formatierungswerte aus dem alten Shape nach der Ersetzung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die **ReplaceLockFormat** -Zelle bestimmt, ob das Master-Shape die lokalen Formatierungswerte der Zellen in den folgenden Abschnitten während einer Form Ersetzung überschreibt: 
  
- Abschnitt " **Fill Format** " 
    
- Abschnitt " **Linien Format** " 
    
- Abschnitt " **Schnellformatvorlage** " 
    
- Abschnitt " **Design Properties** " 
    
- Abschnitt " **Gradient Properties** " 
    
- Abschnitt " **Fase Properties** " 
    
- Abschnitt " **additional Effect Properties** " 
    
- Abschnitt " **Linienverlauf beendet** " 
    
- Abschnitt " **Farbverlaufsstopps** " 
    
Wenn Sie einen Verweis auf die Zelle **ReplaceLockFormat** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockFormat  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ReplaceLockFormat** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockFormat** <br/> |
   

