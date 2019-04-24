---
title: PageLockDuplicate Cell (Page Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Bestimmt, ob die Seite dupliziert werden kann, als boolescher Wert.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283664"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>PageLockDuplicate Cell (Page Properties section)

Bestimmt, ob die Seite dupliziert werden kann, als boolescher Wert.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Duplikate** im Kontextmenü der Seite und die **Page. Duplicate** -Automatisierungsmethode sind beide für die Seite deaktiviert.  <br/> |
|FALSE  <br/> |Die Seite kann dupliziert werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **PageLockDuplicate** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageLockDuplicate  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **PageLockDuplicate** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageLockDuplicate** <br/> |
   

