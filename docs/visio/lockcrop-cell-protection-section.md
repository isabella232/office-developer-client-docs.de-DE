---
title: Zelle "LockCrop" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
ms.localizationpriority: medium
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Sperrt ein Objekt aus einem anderen Programm, damit es nicht mithilfe des Zuschneidetools zugeschnitten werden kann.
ms.openlocfilehash: 0a3224adf6884312c5a722c5b5542a51582a32e3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603641"
---
# <a name="lockcrop-cell-protection-section"></a>Zelle "LockCrop" (Abschnitt "Protection")

Sperrt ein Objekt aus einem anderen Programm, damit es nicht mithilfe des Zuschneidetools zugeschnitten werden kann. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht zugeschnitten werden.  <br/> |
| FALSE  <br/> | Shape kann zugeschnitten werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle "LockCrop" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockCrop  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockCrop anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockCrop** <br/> |
   

