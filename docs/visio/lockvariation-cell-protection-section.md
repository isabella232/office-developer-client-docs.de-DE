---
title: LockVariation Cell (Protection section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Bestimmt, ob die Design Variation, die auf die Seite oder Form angewendet wird, als boolescher Wert geändert werden kann.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358065"
---
# <a name="lockvariation-cell-protection-section"></a>LockVariation Cell (Protection section)

Bestimmt, ob die Design Variation, die auf die Seite oder Form angewendet wird, als boolescher Wert geändert werden kann.
  
|||
|:-----|:-----|
|TRUE  <br/> |Die aktuelle Variation, die auf die Seite oder Form angewendet wird, kann nicht geändert werden.  <br/> |
|FALSE  <br/> |Die Variation der Seite oder Form kann geändert werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **LockVariation** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockVariation  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LockVariation** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockVariation** <br/> |
   

