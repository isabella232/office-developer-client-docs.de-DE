---
title: ReplaceLockText Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben. Die ReplaceLockText bestimmt, ob die Textanzeige auf das Master-Shape den Text der Form, die ersetzt werden überschrieben.
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797858"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>ReplaceLockText Cell (Change Shape Behavior Section)

Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben. Die **ReplaceLockText** bestimmt, ob die Textanzeige auf das Master-Shape den Text der Form, die ersetzt werden überschrieben. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> | Der Text auf das master-Shape überschreibt den Text auf dem alten Shape. Darüber hinaus überschreibt das master-Shape der Werte von Zellen in den folgenden Abschnitten während einer Ersetzungsoperation Form:  <br/> Abschnitt " **Text Fields** "  <br/> Abschnitt " **Text Block Format** "  <br/> |
|FALSE  <br/> |Ersatz-Shapes enthält Text, Textfelder oder andere Texteigenschaften von der alten Form, die mit dem Shape hinzugefügt wurden.  <br/> Ersatz-Shapes Eigenschaften von der alten Form Text enthält, besitzt Ersatz-Shapes auch Werte in den Abschnitten **Zeichen-** und **Absatzformaten** der alten Form, wenn sie mehr als eine Zeile verfügen.  <br/> |
   
Wenn auf TRUE (1), die Werte des Master-Shapes die Werte der folgenden auf die zu ersetzende Form ersetzt:
  
- [Zelle "TheText" (Abschnitt "Events")](thetext-cell-events-section.md)
    
- Zellen im [Abschnitt "Character"](character-section.md)
    
- Zellen im [Abschnitt "Paragraph"](paragraph-section.md)
    
- Zellen im [Abschnitt "Tabs"](tabs-section.md)
    
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **ReplaceLockText** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockText  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ReplaceLockText** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockText** <br/> |
   

