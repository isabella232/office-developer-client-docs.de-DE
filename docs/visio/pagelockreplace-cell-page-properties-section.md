---
title: PageLockReplace Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Gibt an, ob für diese Seite die Schaltfläche Form ersetzen deaktiviert werden soll.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797587"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>PageLockReplace Cell (Page Properties Section)

Gibt an, ob für diese Seite die Schaltfläche **Form ersetzen** deaktiviert werden soll. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die **Form ändern** -Schaltfläche ist nicht verfügbar, wenn diese Seite aktiv ist.  <br/> |
|FALSE  <br/> |Auf dieser Seite wird nicht die Schaltfläche **Form ändern** deaktiviert. Die Schaltfläche kann weiterhin ausgeführt, wenn abgeblendet werden: die **DocLockReplace** auf die **DocumentSheet** auf **TRUE**; festgelegt ist die Zelle **LockReplace** für das ausgewählte Shape wird auf **TRUE**festgelegt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **PageLockReplace** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageLockReplace  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **PageLockReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageLockReplace** <br/> |
   

