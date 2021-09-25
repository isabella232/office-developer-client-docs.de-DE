---
title: Zelle "LockSelect" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
ms.localizationpriority: medium
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Verhindert, dass ein Shape ausgewählt werden kann.
ms.openlocfilehash: 98a0f8151cf2b5b0c08c7a86aec87b8121a9ccb5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573950"
---
# <a name="lockselect-cell-protection-section"></a>Zelle "LockSelect" (Abschnitt "Protection")

Verhindert, dass ein Shape ausgewählt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht ausgewählt werden.  <br/> |
| FALSE  <br/> | Shape kann ausgewählt werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Damit LockSelect wirksam wird, muss das Kontrollkästchen **Shapes** im Dialogfeld **Dokument schützen** aktiviert sein. 
  
Um einen Verweis auf die Zelle "LockSelect" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockSelect  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockSelect anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockSelect** <br/> |
   

