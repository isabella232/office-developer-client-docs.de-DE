---
title: Zelle "PageLockDuplicate" (Abschnitt "Page Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Bestimmt, ob die Seite als boolescher Wert dupliziert werden kann.
ms.openlocfilehash: 41ac55f68993f164ae7e31aad0aab4720d58643e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562937"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>Zelle "PageLockDuplicate" (Abschnitt "Page Properties")

Bestimmt, ob die Seite als boolescher Wert dupliziert werden kann.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Duplizieren** im Kontextmenü der Seite und die **Page.Duplicate-Automatisierungsmethode** sind beide für die Seite deaktiviert.  <br/> |
|FALSE  <br/> |Die Seite kann dupliziert werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle **"PageLockDuplicate"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PageLockDuplicate  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **PageLockDuplicate** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPage** <br/> |
| Zellenindex:  <br/> |**visPageLockDuplicate** <br/> |
   

