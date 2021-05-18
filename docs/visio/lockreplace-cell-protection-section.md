---
title: Zelle "LockReplace" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Gibt an, ob ein Shape an einem Ersetzungsvorgang teilnehmen kann (entweder als Ziel- oder als Ersatzform).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404141"
---
# <a name="lockreplace-cell-protection-section"></a>Zelle "LockReplace" (Abschnitt "Protection")

Gibt an, ob ein Shape an einem Ersetzungsvorgang teilnehmen kann (entweder als Ziel- oder als Ersatzform). 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Shape kann nicht ersetzt oder als Ersatzform verwendet werden.  <br/> Für eine Form auf dem Zeichenbereich wird die Schaltfläche **Shape** ändern deaktiviert, wenn die Form ausgewählt ist.  <br/> Bei einer Form auf einer Schablone wird das Shape nicht  als Ersatzform angezeigt, wenn auf die Schaltfläche Shape ändern geklickt wird.  <br/> |
|FALSE  <br/> |Das Shape kann ersetzt oder als Ersatzform verwendet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LockReplace** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockReplace  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle LockReplace** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockReplace** <br/> |
   

