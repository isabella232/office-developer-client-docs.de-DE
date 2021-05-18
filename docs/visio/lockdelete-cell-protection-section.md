---
title: Zelle "LockDelete" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Sperrt das Shape, damit es nicht gelöscht werden kann.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423139"
---
# <a name="lockdelete-cell-protection-section"></a>Zelle "LockDelete" (Abschnitt "Protection")

Sperrt das Shape, damit es nicht gelöscht werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht gelöscht werden.  <br/> |
| FALSE  <br/> | Shape kann gelöscht werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle LockDelete anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockDelete  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockDelete nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockDelete** <br/> |
   

