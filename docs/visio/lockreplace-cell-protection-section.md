---
title: Zelle "LockReplace" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Gibt an, ob ein Shape an einem Ersetzungsvorgang teilnehmen kann (als Ziel oder als Ersatz-Shape).
ms.openlocfilehash: e5220d0d9031aaa383a5dadd4c0c4049ec427eb0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573964"
---
# <a name="lockreplace-cell-protection-section"></a>Zelle "LockReplace" (Abschnitt "Protection")

Gibt an, ob ein Shape an einem Ersetzungsvorgang teilnehmen kann (als Ziel oder als Ersatz-Shape). 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Form kann nicht ersetzt oder als Ersatzform verwendet werden.  <br/> Bei einem Shape auf dem Zeichenbereich ist die Schaltfläche **"Shape ändern"** deaktiviert, wenn das Shape ausgewählt ist.  <br/> Bei einem Shape in einer Schablone wird das Shape nicht als Ersatzform angezeigt, wenn auf die Schaltfläche **"Shape ändern"** geklickt wird.  <br/> |
|FALSE  <br/> |Die Form kann ersetzt oder als Ersatzform verwendet werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die **Zelle LockReplace** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockReplace  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **LockReplace** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockReplace** <br/> |
   

