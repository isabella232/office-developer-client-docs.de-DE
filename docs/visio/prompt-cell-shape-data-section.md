---
title: Zelle "Prompt" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
ms.localizationpriority: medium
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster Shape-Daten platziert wird.
ms.openlocfilehash: d99886f28562fad348eb76119e06b9092072c76e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607983"
---
# <a name="prompt-cell-shape-data-section"></a>Zelle "Prompt" (Abschnitt "Shape Data")

Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster **Shape-Daten** platziert wird. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Eingabeaufforderungszelle anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . Eingabeaufforderung, wobei  *Name*  der Zeilenname ist  <br/> |
   
Um einen Verweis auf die Eingabeaufforderungszelle anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp +** *i*  where  *i*  = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsPrompt** <br/> |
   

