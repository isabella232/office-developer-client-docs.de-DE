---
title: Zelle "LockThemeIndex" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Verhindert, dass die Zelle "ThemeIndex" in der Zeile "Designeigenschaften" geändert wird, indem ein neues Design angewendet oder ein neues Konnektorschema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten.
ms.openlocfilehash: c0f58df4220e309017f3846f7d8060c71cb4ba9f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582568"
---
# <a name="lockthemeindex-cell-protection-section"></a>Zelle "LockThemeIndex" (Abschnitt "Protection")

Verhindert, dass die Zelle **"ThemeIndex"** in der Zeile **"Designeigenschaften"** geändert wird, indem ein neues Design angewendet oder ein neues Konnektorschema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Zelle **"ThemeIndex"** kann nicht vom aktuellen Wert geändert werden, es sei denn, sie wird direkt im ShapeSheet geändert.  <br/> |
|FALSE  <br/> |Die Zelle **"ThemeIndex"** kann vom aktuellen Wert geändert werden, wenn das Design geändert wird.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die **Zelle "LockThemeIndex"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockThemeIndex  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **LockThemeIndex** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockThemeIndex** <br/> |
   

