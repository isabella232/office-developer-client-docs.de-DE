---
title: Zelle "ReplaceLockText" (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shape-Ersetzungsvorgangs ersetzt wird. ReplaceLockText bestimmt, ob der im Master-Shape angezeigte Text den Text der zu ersetzenden Form überschreibt.
ms.openlocfilehash: f0ddee2e50750ec91c811d409d507767258f45f4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570183"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>Zelle "ReplaceLockText" (Abschnitt "Change Shape Behavior")

Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shape-Ersetzungsvorgangs ersetzt wird. **ReplaceLockText** bestimmt, ob der im Master-Shape angezeigte Text den Text der zu ersetzenden Form überschreibt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> | Der Text in der Masterform überschreibt den Text der alten Form. Darüber hinaus überschreibt das Master-Shape während eines Shape-Ersetzungsvorgangs die Werte der Zellen in den folgenden Abschnitten:  <br/> Abschnitt **"Text Fields"**  <br/> Abschnitt **"Text Block Format"**  <br/> |
|FALSE  <br/> |Die Ersetzungsform enthält alle Text-, Textfelder- oder anderen Texteigenschaften aus der alten Form, die der Form hinzugefügt wurden.  <br/> Wenn die Ersetzungsform Texteigenschaften aus der alten Form enthält, enthält die Ersetzungsform auch die Werte aus den Abschnitten **"Character"** und **"Paragraph"** der alten Form, wenn sie mehr als eine Zeile haben.  <br/> |
   
Bei Festlegung auf TRUE (1) werden die Werte des Shape-Master-Shapes durch die Werte des folgenden Shapes ersetzt, das ersetzt wird:
  
- [Zelle "TheText" (Abschnitt "Events")](thetext-cell-events-section.md)
    
- Zellen im [Abschnitt "Character"](character-section.md)
    
- Zellen im [Abschnitt "Paragraph"](paragraph-section.md)
    
- Zellen im [Abschnitt "Tabs"](tabs-section.md)
    
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die **Zelle "ReplaceLockText"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockText  <br/> |
   
Um einen Verweis auf die Zelle **"ReplaceLockText"** anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockText** <br/> |
   

