---
title: Zelle "LockDelete" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
ms.localizationpriority: medium
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Sperrt das Shape, damit es nicht gelöscht werden kann.
ms.openlocfilehash: dc746ae96dc5f8d359b1f7500b59fdbe7d7d86f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554467"
---
# <a name="lockdelete-cell-protection-section"></a>Zelle "LockDelete" (Abschnitt "Protection")

Sperrt das Shape, damit es nicht gelöscht werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht gelöscht werden.  <br/> |
| FALSE  <br/> | Shape kann gelöscht werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "LockDelete" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockDelete  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockDelete anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockDelete** <br/> |
   

