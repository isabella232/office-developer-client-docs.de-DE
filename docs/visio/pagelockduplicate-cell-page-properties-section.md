---
title: Zelle "PageLockDuplicate" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Bestimmt, ob die Seite als boolescher Wert dupliziert werden kann.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425981"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>Zelle "PageLockDuplicate" (Abschnitt "Page Properties")

Bestimmt, ob die Seite als boolescher Wert dupliziert werden kann.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Duplikate** im Kontextmenü der Seite und die **Page.Duplicate-Automatisierungsmethode** sind beide für die Seite deaktiviert.  <br/> |
|FALSE  <br/> |Die Seite kann dupliziert werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die **Zelle PageLockDuplicate** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageLockDuplicate  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **PageLockDuplicate-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageLockDuplicate** <br/> |
   

