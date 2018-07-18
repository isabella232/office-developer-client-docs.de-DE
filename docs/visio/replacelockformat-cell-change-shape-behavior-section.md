---
title: ReplaceLockFormat Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben. Wenn die Zelle ReplaceLockFormat eines master-Shapes (1) "true" festgelegt ist, überschreiben die Formatierung Werte des Master-Shapes alle entsprechenden Werte eines Shapes, die durch das Master-Shape ersetzt wird.
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797825"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a>ReplaceLockFormat Cell (Change Shape Behavior Section)

Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben. Wenn die Zelle **ReplaceLockFormat** eines master-Shapes (1) "true" festgelegt ist, überschreiben die Formatierung Werte des Master-Shapes alle entsprechenden Werte eines Shapes, die durch das Master-Shape ersetzt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Wenn die Zelle **ReplaceLockFormat** eines master-Shapes auf TRUE festgelegt ist, überschreiben die Formatierung Werte des Master-Shapes alle entsprechenden Werte eines Shapes, die durch das Master-Shape ersetzt wird.  <br/> |
|FALSE  <br/> |Wenn die Zelle **ReplaceLockFormat** eines master-Shapes auf FALSE festgelegt ist, enthält Ersatz-Shapes die Werte der lokalen Formatierung von der alten Form nach der Ersetzung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Zelle **ReplaceLockFormat** bestimmt, ob das master-Shape der lokalen Formatierung Werte von Zellen in den folgenden Abschnitten während einer Form Ersetzungsvorgang überschreibt: 
  
- Abschnitt " **Fill Format** " 
    
- Abschnitt " **Line Format** " 
    
- **Schnellformatvorlagen** -Abschnitt 
    
- Abschnitt **Design-Eigenschaften** 
    
- **Farbverlauf Eigenschaften** im Abschnitt 
    
- Im Abschnitt **Eigenschaften für die Abschrägung** 
    
- **Zusätzliche Eigenschaften von Animationseffekten** -Abschnitt 
    
- **Zeile Farbverlaufstopps** -Abschnitt 
    
- **Füllen Sie Farbverlaufstopps** -Abschnitt 
    
Wenn Sie einen Verweis auf die Zelle **ReplaceLockFormat** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockFormat  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ReplaceLockFormat** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockFormat** <br/> |
   

