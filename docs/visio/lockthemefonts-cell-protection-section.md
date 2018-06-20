---
title: LockThemeFonts Cell (Protection Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Verhindert, dass die FontIndex Zelle in der Zeile mit Design anwenden eines neuen Designs geändert werden. Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797422"
---
# <a name="lockthemefonts-cell-protection-section"></a>LockThemeFonts Cell (Protection Section)

Verhindert, dass die **FontIndex** Zelle in der Zeile mit **Design** Anwenden eines neuen Designs geändert werden. Verhindert nicht, dass Benutzer diesen Wert in das ShapeSheet manuell zu bearbeiten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Zelle **FontIndex** kann nicht aus dem aktuellen Wert geändert werden, sofern nicht direkt im ShapeSheet geändert.  <br/> |
|FALSE  <br/> |Die Zelle **FontIndex** kann vom aktuellen Wert geändert werden, wenn das Design geändert wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **LockThemeFonts** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockThemeFonts  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LockThemeFonts** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockThemeFonts** <br/> |
   

