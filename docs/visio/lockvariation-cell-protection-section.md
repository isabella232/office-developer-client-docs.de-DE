---
title: Zelle "LockVariation" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Bestimmt, ob die auf die Seite oder form angewendete Designvariante als boolescher Wert geändert werden kann.
ms.openlocfilehash: eac661fd88e53fa42999ba5e1e23af8bc113e4bf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573922"
---
# <a name="lockvariation-cell-protection-section"></a>Zelle "LockVariation" (Abschnitt "Protection")

Bestimmt, ob die auf die Seite oder form angewendete Designvariante als boolescher Wert geändert werden kann.
  
|||
|:-----|:-----|
|TRUE  <br/> |Die aktuelle Abweichung, die auf das Zeichenblatt oder die Form angewendet wird, kann nicht geändert werden.  <br/> |
|FALSE  <br/> |Die Variation des Zeichenblatts oder der Form kann geändert werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die **Zelle "LockVariation"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockVariation  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **LockVariation** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockVariation** <br/> |
   

