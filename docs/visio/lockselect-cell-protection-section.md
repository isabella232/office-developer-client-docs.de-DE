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
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797403"
---
# <a name="lockselect-cell-protection-section"></a>LockSelect Cell (Protection Section)

Verhindert, dass ein Shape ausgewählt werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht ausgewählt werden.  <br/> |
| FALSE  <br/> | Shape kann ausgewählt werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Damit LockSelect wirksam wird, muss das Kontrollkästchen Shapes im Dialogfeld Dokument schützen aktiviert werden. 
  
Wenn Sie einen Verweis auf die Zelle LockSelect aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockSelect  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LockSelect aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockSelect** <br/> |
   

