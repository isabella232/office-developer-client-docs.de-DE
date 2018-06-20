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
ms.openlocfilehash: 2b25d1d9b00d062214c02c3fc7b14569b43a5110
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798208"
---
# <a name="strikethru-cell-character-section"></a>Zelle "Strikethru" (Abschnitt "Character")

Legt fest, ob der Text als durchgestrichen formatiert ist.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Text ist als durchgestrichen formatiert.  <br/> |
|FALSE  <br/> |Text ist nicht als durchgestrichen formatiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie auf der Registerkarte **Start** auf den Pfeil neben **Schriftart** ). 
  
Wenn Sie einen Verweis auf die Zelle Strikethru nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.Strikethru [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Strikethru aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterStrikethru** <br/> |
   

