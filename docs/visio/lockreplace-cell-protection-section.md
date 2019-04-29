---
title: LockReplace Cell (Protection section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Gibt an, ob ein Shape an einem Ersetzungsvorgang (als Ziel-oder als Ersatz-Shape) teilnehmen kann.
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404141"
---
# <a name="lockreplace-cell-protection-section"></a>LockReplace Cell (Protection section)

Gibt an, ob ein Shape an einem Ersetzungsvorgang (als Ziel-oder als Ersatz-Shape) teilnehmen kann. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Shape kann nicht ersetzt oder als Ersatzform verwendet werden.  <br/> Bei einem Shape auf dem Canvas ist die Schaltfläche **Shape ändern** deaktiviert, wenn das Shape ausgewählt ist.  <br/> Bei einem Shape auf einer Schablone wird das Shape nicht als Ersatzform angezeigt, wenn auf die Schaltfläche **Shape ändern** geklickt wird.  <br/> |
|FALSE  <br/> |Die Form kann ersetzt oder als Ersatzform verwendet werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **LockReplace** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockReplace  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LockReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockReplace** <br/> |
   

