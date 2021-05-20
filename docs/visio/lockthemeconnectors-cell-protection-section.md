---
title: Zelle "LockThemeConnectors" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: Verhindert, dass die Zelle ConnectorsSchemeIndex in der Zeile Designeigenschaften geändert wird, indem ein neues Design angewendet oder ein neues Verbindungsschema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten.
ms.openlocfilehash: 8097e50646fd59f4ac0212cbe9ca2ecfaadab7a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438407"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>Zelle "LockThemeConnectors" (Abschnitt "Protection")

Verhindert, **dass die Zelle ConnectorsSchemeIndex** in der Zeile **Designeigenschaften** geändert wird, indem ein neues Design angewendet oder ein neues Verbindungsschema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die **Zelle ConnectorsSchemeIndex** kann nicht vom aktuellen Wert geändert werden, es sei denn, sie wird direkt im ShapeSheet geändert.  <br/> |
|FALSE  <br/> |Die **Zelle ConnectorsSchemeIndex** kann über die Benutzeroberfläche von ihrem aktuellen Wert geändert werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LockThemeConnectors** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockThemeConnectors  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle LockThemeConnectors** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockThemeConnectors** <br/> |
   

