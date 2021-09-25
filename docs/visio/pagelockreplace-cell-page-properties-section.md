---
title: Zelle "PageLockReplace" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Gibt an, ob die Schaltfläche "Shape ersetzen" für diese Seite deaktiviert werden soll.
ms.openlocfilehash: 7dff941f3761cd4bf022e9e1ad42ff9aa5a6154d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554243"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>Zelle "PageLockReplace" (Abschnitt "Page Properties")

Gibt an, ob die Schaltfläche **"Shape ersetzen"** für diese Seite deaktiviert werden soll. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Schaltfläche **"Shape ändern"** ist ausgegraut, wenn diese Seite aktiv ist.  <br/> |
|FALSE  <br/> |Die Schaltfläche **"Shape ändern"** ist von dieser Seite nicht deaktiviert. Die Schaltfläche ist möglicherweise weiterhin ausgegraut, wenn: **DocLockReplace** im **DocumentSheet** auf **TRUE** festgelegt ist; Die Zelle **LockReplace** für das ausgewählte Shape ist auf **TRUE** festgelegt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "PageLockReplace"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageLockReplace  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **PageLockReplace** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageLockReplace** <br/> |
   

