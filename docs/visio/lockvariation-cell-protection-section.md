---
title: Zelle "LockVariation" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Bestimmt, ob die auf die Seite oder Form angewendete Designvariation als boolescher Wert geändert werden kann.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427927"
---
# <a name="lockvariation-cell-protection-section"></a>Zelle "LockVariation" (Abschnitt "Protection")

Bestimmt, ob die auf die Seite oder Form angewendete Designvariation als boolescher Wert geändert werden kann.
  
|||
|:-----|:-----|
|TRUE  <br/> |Die aktuelle Variation, die auf die Seite oder Form angewendet wird, kann nicht geändert werden.  <br/> |
|FALSE  <br/> |Die Variation der Seite oder Form kann geändert werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LockVariation** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockVariation  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **LockVariation-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockVariation** <br/> |
   

