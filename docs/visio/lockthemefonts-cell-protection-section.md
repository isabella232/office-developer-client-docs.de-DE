---
title: LockThemeFonts Cell (Protection section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Verhindert, dass die Zelle FontIndex in der Zeile Designeigenschaften durch Anwenden eines neuen Designs geändert wird. Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421228"
---
# <a name="lockthemefonts-cell-protection-section"></a>LockThemeFonts Cell (Protection section)

Verhindert, dass die Zelle **FontIndex** in der Zeile **Designeigenschaften** durch Anwenden eines neuen Designs geändert wird. Verhindert nicht, dass Benutzer diesen Wert manuell im ShapeSheet bearbeiten. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Zelle **FontIndex** kann nicht von Ihrem aktuellen Wert geändert werden, es sei denn, Sie wurde direkt im ShapeSheet geändert.  <br/> |
|FALSE  <br/> |Die Zelle **FontIndex** kann vom aktuellen Wert geändert werden, wenn das Design geändert wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **LockThemeFonts** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockThemeFonts  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **LockThemeFonts** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockThemeFonts** <br/> |
   

