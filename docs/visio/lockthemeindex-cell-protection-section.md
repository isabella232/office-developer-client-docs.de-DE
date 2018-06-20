---
title: LockThemeIndex Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Verhindert, dass ThemeIndex-Zelle in der Zeile mit Komponenteneigenschaften Design durch Anwenden eines neuen Designs oder Auswählen eines neuen Connector Schemas geändert wird. Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797404"
---
# <a name="lockthemeindex-cell-protection-section"></a>LockThemeIndex Cell (Protection Section)

Verhindert, dass **ThemeIndex** -Zelle in der Zeile mit **Komponenteneigenschaften Design** durch Anwenden eines neuen Designs oder Auswählen eines neuen Connector Schemas geändert wird. Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Zelle **ThemeIndex** kann nicht aus dem aktuellen Wert geändert werden, sofern nicht direkt im ShapeSheet geändert.  <br/> |
|FALSE  <br/> |Die Zelle **ThemeIndex** kann vom aktuellen Wert geändert werden, wenn das Design geändert wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **LockThemeIndex** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockThemeIndex  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LockThemeIndex** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockThemeIndex** <br/> |
   

