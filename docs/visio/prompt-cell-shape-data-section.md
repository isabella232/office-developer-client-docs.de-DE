---
title: Zelle "Prompt" (Abschnitt "Shape Data")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster Shape-Daten platziert wird.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405485"
---
# <a name="prompt-cell-shape-data-section"></a>Zelle "Prompt" (Abschnitt "Shape Data")

Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster **Shape-Daten** platziert wird. 
  
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle Eingabeaufforderung anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prop.  *Name*  . Eingabeaufforderung, bei der  *Name*  der Zeilenname ist  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Prompt nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionProp** <br/> |
| Zeilenindex:  <br/> |**visRowProp +** *i*  where  *i*  = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCustPropsPrompt** <br/> |
   

