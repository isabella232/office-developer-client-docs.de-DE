---
title: Zelle "Font" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: Stellt die Nummer der Schriftart dar, die zum Formatieren des Texts verwendet wird. Schriftartnummern können abhängig von den auf Ihrem System installierten Schriftarten variieren. Die Nummer 0 stellt die Standardschriftart dar, bei der es sich i. A. um die Schriftart Arial handelt.
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438666"
---
# <a name="font-cell-character-section"></a>Zelle "Font" (Abschnitt "Character")

Stellt die Nummer der Schriftart dar, die zum Formatieren des Texts verwendet wird. Schriftartnummern können abhängig von den auf Ihrem System installierten Schriftarten variieren. Die Nummer 0 stellt die Standardschriftart dar, bei der es sich i. A. um die Schriftart Arial handelt.
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle Font anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Char.Font[  *i*  ] wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Font nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
| Zeilenindex:  <br/> |**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCharacterFont** <br/> |
   

