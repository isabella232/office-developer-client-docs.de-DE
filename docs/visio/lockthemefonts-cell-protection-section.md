---
title: Zelle "LockThemeFonts" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Verhindert, dass die Zelle FontIndex in der Zeile Designeigenschaften geändert wird, indem ein neues Design angewendet wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421228"
---
# <a name="lockthemefonts-cell-protection-section"></a>Zelle "LockThemeFonts" (Abschnitt "Protection")

Verhindert, **dass die Zelle FontIndex** in der Zeile **Designeigenschaften** geändert wird, indem ein neues Design angewendet wird. Verhindert nicht, dass Benutzer diesen Wert im ShapeSheet manuell bearbeiten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die **Zelle FontIndex** kann nicht vom aktuellen Wert geändert werden, es sei denn, sie wird direkt im ShapeSheet geändert.  <br/> |
|FALSE  <br/> |Die **Zelle FontIndex** kann von ihrem aktuellen Wert geändert werden, wenn das Design geändert wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LockThemeFonts** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockThemeFonts  <br/> |
   
Um einen Verweis auf die **Zelle LockThemeFonts** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockThemeFonts** <br/> |
   

