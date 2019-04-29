---
title: Zelle "Strikethru" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Legt fest, ob der Text als durchgestrichen formatiert ist.
ms.openlocfilehash: 4a58123814a4782c279a36d202e1293ec222ef93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412429"
---
# <a name="strikethru-cell-character-section"></a>Zelle "Strikethru" (Abschnitt "Character")

Legt fest, ob der Text als durchgestrichen formatiert ist.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Text ist als durchgestrichen formatiert.  <br/> |
|FALSE  <br/> |Text ist nicht als durchgestrichen formatiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**). 
  
Wenn Sie einen Verweis auf die Zelle Strikethru aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char. Strikethru [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Strikethru aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterStrikethru** <br/> |
   

