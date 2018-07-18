---
title: LockReplace Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Gibt an, ob eine Form einen Ersetzungsvorgang (als ein Ziel oder ein Replacement-Shape) teilnehmen kann.
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797384"
---
# <a name="lockreplace-cell-protection-section"></a>LockReplace Cell (Protection Section)

Gibt an, ob eine Form einen Ersetzungsvorgang (als ein Ziel oder ein Replacement-Shape) teilnehmen kann. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Das Shape kann nicht ersetzt werden oder als Ersatz-Shape verwendet werden.  <br/> Für ein Shape auf die Canvas ist die Schaltfläche **Form ändern** deaktiviert, wenn ein Shape ausgewählt wird.  <br/> Für ein Shape in einer Schablone wird die Form nicht als Ersatz-Shape angezeigt, wenn die **Form ändern** Schaltfläche geklickt wird.  <br/> |
|FALSE  <br/> |Das Shape kann ersetzt oder als Ersatz-Shape verwendet werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **LockReplace** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockReplace  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LockReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockReplace** <br/> |
   

