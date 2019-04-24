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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360669"
---
# <a name="lockselect-cell-protection-section"></a>Zelle "LockSelect" (Abschnitt "Protection")

Verhindert, dass ein Shape ausgewählt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht ausgewählt werden.  <br/> |
| FALSE  <br/> | Shape kann ausgewählt werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Damit die "LockSelect wirksam wird, muss das Kontrollkästchen **Shapes** im Dialogfeld **Dokument schützen** aktiviert sein. 
  
Wenn Sie einen Verweis auf die Zelle "LockSelect aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "LockSelect  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "LockSelect aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockSelect** <br/> |
   

