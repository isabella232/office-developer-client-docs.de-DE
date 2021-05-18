---
title: Zelle ReplaceLockText (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird. Der ReplaceLockText bestimmt, ob der im Master angezeigte Text den Text der zu ersetzenden Form überschreibt.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411918"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>Zelle ReplaceLockText (Abschnitt "Change Shape Behavior")

Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird. Der **ReplaceLockText** bestimmt, ob der im Master angezeigte Text den Text der zu ersetzenden Form überschreibt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> | Der Text auf der Masterform überschreibt den Text auf der alten Form. Darüber hinaus überschreibt die Masterform während eines Shapeersetzungsvorgangs die Werte der Zellen in den folgenden Abschnitten:  <br/> **Abschnitt "Text Fields"**  <br/> **Abschnitt "Text Block Format"**  <br/> |
|FALSE  <br/> |Die Ersetzungsform enthält beliebige Text-, Textfeld- oder andere Texteigenschaften aus der alten Form, die der Form hinzugefügt wurden.  <br/> Wenn die Ersetzungsform Texteigenschaften aus der alten Form enthält, enthält die Ersetzungsform auch die Werte aus den Abschnitten **Character** und **Paragraph** der alten Form, wenn sie mehr als eine Zeile enthalten.  <br/> |
   
Wenn true (1) festgelegt ist, werden durch die Werte des ShapeMasters die folgenden Werte für die ersetzte Form ersetzt:
  
- [Zelle "TheText" (Abschnitt "Events")](thetext-cell-events-section.md)
    
- Zellen im [Abschnitt "Character"](character-section.md)
    
- Zellen im [Abschnitt Absatz](paragraph-section.md)
    
- Zellen im [Abschnitt Registerkarten](tabs-section.md)
    
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die **Zelle ReplaceLockText** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockText  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ReplaceLockText** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockText** <br/> |
   

