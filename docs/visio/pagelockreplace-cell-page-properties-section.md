---
title: PageLockReplace Cell (Page Properties section)
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
# <a name="pagelockreplace-cell-page-properties-section"></a>PageLockReplace Cell (Page Properties section)

Gibt an, ob die Schaltfläche **Shape ersetzen** für diese Seite deaktiviert werden soll. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Schaltfläche **Shape ändern** ist ausgeblendet, wenn diese Seite aktiv ist.  <br/> |
|FALSE  <br/> |Die Schaltfläche **Shape ändern** ist von dieser Seite nicht deaktiviert. Die Schaltfläche ist möglicherweise noch abgeblendet, wenn: der **DocLockReplace** auf dem **DocumentSheet** auf **true**festgelegt ist; die **LockReplace** -Zelle für die ausgewählte Form ist auf **true**festgelegt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **PageLockReplace** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageLockReplace  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **PageLockReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageLockReplace** <br/> |
   

