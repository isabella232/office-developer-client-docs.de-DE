---
title: Zelle "LockSelect" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Verhindert, dass ein Shape ausgewählt werden kann.
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409755"
---
# <a name="lockselect-cell-protection-section"></a>Zelle "LockSelect" (Abschnitt "Protection")

Verhindert, dass ein Shape ausgewählt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht ausgewählt werden.  <br/> |
| FALSE  <br/> | Shape kann ausgewählt werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Damit LockSelect wirksam wird, muss das Kontrollkästchen **Shapes** im Dialogfeld Dokument **schützen** aktiviert sein. 
  
Um einen Verweis auf die Zelle LockSelect anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockSelect  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockSelect nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockSelect** <br/> |
   

