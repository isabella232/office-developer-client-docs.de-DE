---
title: Zelle "PageLockReplace" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Gibt an, ob die Schaltfläche Shape ersetzen für diese Seite deaktiviert werden soll.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433101"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>Zelle "PageLockReplace" (Abschnitt "Page Properties")

Gibt an, **ob** die Schaltfläche Shape ersetzen für diese Seite deaktiviert werden soll. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die **Schaltfläche Shape ändern** ist ausgegraut, wenn diese Seite aktiv ist.  <br/> |
|FALSE  <br/> |Die **Schaltfläche Shape ändern** wird von dieser Seite nicht deaktiviert. Die Schaltfläche ist möglicherweise noch abgeblendet, wenn: **DocLockReplace** im **DocumentSheet** auf **TRUE festgelegt ist;** Die **Zelle LockReplace** für die ausgewählte Form ist auf **TRUE festgelegt.**  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die **Zelle PageLockReplace** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageLockReplace  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **PageLockReplace-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageLockReplace** <br/> |
   

