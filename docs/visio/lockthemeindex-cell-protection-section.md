---
title: LockThemeIndex Cell (Protection section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Verhindert, dass die ThemeIndex Zelle in Designeigenschaften Zeile geändert wird, indem ein neues Design angewendet oder ein neues Connector-Schema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411239"
---
# <a name="lockthemeindex-cell-protection-section"></a>LockThemeIndex Cell (Protection section)

Verhindert, dass die **ThemeIndex** Zelle in **Designeigenschaften** Zeile geändert wird, indem ein neues Design angewendet oder ein neues Connector-Schema ausgewählt wird. Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Zelle **ThemeIndex** kann nicht von Ihrem aktuellen Wert geändert werden, es sei denn, Sie wurde direkt im ShapeSheet geändert.  <br/> |
|FALSE  <br/> |Die Zelle **ThemeIndex** kann vom aktuellen Wert geändert werden, wenn das Design geändert wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **LockThemeIndex** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockThemeIndex  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LockThemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockThemeIndex** <br/> |
   

