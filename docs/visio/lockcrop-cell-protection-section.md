---
title: Zelle "LockCrop" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Sperrt ein Objekt aus einem anderen Programm, damit es nicht mithilfe des Zuschneidetools zugeschnitten werden kann.
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411855"
---
# <a name="lockcrop-cell-protection-section"></a>Zelle "LockCrop" (Abschnitt "Protection")

Sperrt ein Objekt aus einem anderen Programm, damit es nicht mithilfe des Zuschneidetools zugeschnitten werden kann. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht zugeschnitten werden.  <br/> |
| FALSE  <br/> | Shape kann zugeschnitten werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle LockCrop anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockCrop  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LockCrop-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockCrop** <br/> |
   

