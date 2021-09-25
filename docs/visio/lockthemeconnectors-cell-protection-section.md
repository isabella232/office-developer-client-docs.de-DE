---
title: Zelle "LockThemeConnectors" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Verhindert, dass die Zelle ConnectorsSchemeIndex in der Zeile Designeigenschaften geändert wird, indem ein neues Design angewendet oder ein neues Konnektorschema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten.
ms.openlocfilehash: 3e1fd7571795bb5fea7cb4d0a5f8da091b5b7783
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554397"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>Zelle "LockThemeConnectors" (Abschnitt "Protection")

Verhindert, dass die Zelle **ConnectorsSchemeIndex** in der Zeile Designeigenschaften geändert wird, indem ein neues Design angewendet oder ein neues Konnektorschema ausgewählt wird.  Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die **Zelle ConnectorsSchemeIndex** kann nicht vom aktuellen Wert geändert werden, es sei denn, sie wird direkt im ShapeSheet geändert.  <br/> |
|FALSE  <br/> |Die Zelle **"ConnectorsSchemeIndex"** kann über die Benutzeroberfläche vom aktuellen Wert geändert werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle **"LockThemeConnectors"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockThemeConnectors  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **LockThemeConnectors** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockThemeConnectors** <br/> |
   

