---
title: Zelle "Case" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: Bestimmt die Groß- und Kleinschreibung für den Text des Shapes. Die Optionen Nur Großbuchstaben (1) und Große Anfangsbuchstaben (2) ändern die Darstellung eines komplett in Großbuchstaben eingegebenen Texts nicht. Der Text muss in Kleinbuchstaben eingegeben werden, damit diese Optionen eine Wirkung zeigen.
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434347"
---
# <a name="case-cell-character-section"></a>Zelle "Case" (Abschnitt "Character")

Bestimmt die Groß- und Kleinschreibung für den Text des Shapes. Die Optionen Nur Großbuchstaben (1) und Große Anfangsbuchstaben (2) ändern die Darstellung eines komplett in Großbuchstaben eingegebenen Texts nicht. Der Text muss in Kleinbuchstaben eingegeben werden, damit diese Optionen eine Wirkung zeigen.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Normalschreibung  <br/> |**visCaseNormal** <br/> |
| 1  <br/> | Nur Großbuchstaben  <br/> |**visCaseAllCaps** <br/> |
| 2  <br/> | Große Anfangsbuchstaben  <br/> |**visCaseInitialCaps** <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle Case anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Char.Case[  *i*  ] where  *i*  = <1>, 2, 3, ...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Case nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
| Zeilenindex:  <br/> |**visRowCharacter**  +   *i* where *i* = 0, 1, 2, ...  <br/> |
| Zellenindex:  <br/> |**visCharacterCase** <br/> |
   

