---
title: Zelle "DoubleStrikethrough" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Legt fest, ob der Text doppelt durchgestrichen formatiert ist.
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360592"
---
# <a name="doublestrikethrough-cell-character-section"></a>Zelle "DoubleStrikethrough" (Abschnitt "Character")

Legt fest, ob der Text doppelt durchgestrichen formatiert ist.
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle DoubleStrikethrough anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Char.DoubleStrikethrough[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DoubleStrikethrough-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
| Zeilenindex:  <br/> |**visRowCharacter**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visCharacterDoubleStrikethrough** <br/> |
   

