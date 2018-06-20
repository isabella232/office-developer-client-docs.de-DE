---
title: LockVariation Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Bestimmt, ob die Design-Variante, die auf dem Zeichenblatt oder Shape angewendet, als ein boolescher Wert, geändert werden kann.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797418"
---
# <a name="lockvariation-cell-protection-section"></a>LockVariation Cell (Protection Section)

Bestimmt, ob die Design-Variante, die auf dem Zeichenblatt oder Shape angewendet, als ein boolescher Wert, geändert werden kann.
  
|||
|:-----|:-----|
|TRUE  <br/> |Die aktuelle Variation auf dem Zeichenblatt oder Shape angewendet kann nicht geändert werden.  <br/> |
|FALSE  <br/> |Die Variante des Zeichenblatts oder des Shape kann geändert werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **LockVariation** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockVariation  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LockVariation** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockVariation** <br/> |
   

