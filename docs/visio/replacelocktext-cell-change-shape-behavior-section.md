---
title: Zelle "ReplaceLockText" (Abschnitt "Shape-Verhalten ändern")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird. Die ReplaceLockText bestimmt, ob der Text, der im Master angezeigt wird, den Text der Form überschreibt, die ersetzt wird.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348202"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a>Zelle "ReplaceLockText" (Abschnitt "Shape-Verhalten ändern")

Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird. Die **ReplaceLockText** bestimmt, ob der Text, der im Master angezeigt wird, den Text der Form überschreibt, die ersetzt wird. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> | Der Text im Master-Shape überschreibt den Text auf dem alten Shape. Außerdem überschreibt das Master-Shape die Werte der Zellen in den folgenden Abschnitten während eines Form Ersetzungsvorgangs:  <br/> Abschnitt " **Text Fields** "  <br/> Abschnitt " **Text Block Format** "  <br/> |
|FALSE  <br/> |Die Ersatzform enthält Text, Textfelder oder andere Texteigenschaften aus dem alten Shape, die dem Shape hinzugefügt wurden.  <br/> Wenn die Ersatzform Texteigenschaften aus dem alten Shape enthält, weist die Ersatzform auch die Werte aus den **Zeichen** -und **Absatz** Abschnitten der alten Form auf, wenn Sie mehr als eine Zeile aufweisen.  <br/> |
   
Bei Festlegung auf "TRUE" (1) werden durch die Werte des Shape-Masters die folgenden Werte für das zu ersetzende Shape ersetzt:
  
- [Zelle "TheText" (Abschnitt "Events")](thetext-cell-events-section.md)
    
- Zellen im [Abschnitt "Character"](character-section.md)
    
- Zellen im [Abschnitt "Paragraph"](paragraph-section.md)
    
- Zellen im [Abschnitt "Tabs"](tabs-section.md)
    
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **ReplaceLockText** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ReplaceLockText  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ReplaceLockText** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowReplaceBehaviors** <br/> |
| Zellenindex:  <br/> |**visReplaceLockText** <br/> |
   

