---
title: Zelle "LockThemeIndex" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Verhindert, dass die Zelle ThemeIndex in der Zeile Designeigenschaften geändert wird, indem ein neues Design angewendet oder ein neues Connectorschema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411239"
---
# <a name="lockthemeindex-cell-protection-section"></a>Zelle "LockThemeIndex" (Abschnitt "Protection")

Verhindert, dass **die Zelle ThemeIndex** in der **Zeile Designeigenschaften** geändert wird, indem ein neues Design angewendet oder ein neues Connectorschema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die **Zelle ThemeIndex** kann nicht vom aktuellen Wert geändert werden, es sei denn, sie wird direkt im ShapeSheet geändert.  <br/> |
|FALSE  <br/> |Die **Zelle ThemeIndex** kann von ihrem aktuellen Wert geändert werden, wenn das Design geändert wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LockThemeIndex** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockThemeIndex  <br/> |
   
Um einen Verweis auf die **Zelle LockThemeIndex nach Index** aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockThemeIndex** <br/> |
   

