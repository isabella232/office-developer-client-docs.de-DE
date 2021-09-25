---
title: Zelle "DocLockDuplicatePage" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Bestimmt, ob Seiten im Dokument als boolescher Wert dupliziert werden können.
ms.openlocfilehash: 264b55909a5eb48636601566d6392e62393f00d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559920"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>Zelle "DocLockDuplicatePage" (Abschnitt "Document Properties")

Bestimmt, ob Seiten im Dokument als boolescher Wert dupliziert werden können.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Duplizieren** im Kontextmenü der Seite und die **Page.Duplicate-Automatisierungsmethode** sind beide deaktiviert.  <br/> |
|FALSE  <br/> |Die Seite kann dupliziert werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die **Zelle DocLockDuplicatePage** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DocLockDuplicatePage  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **DocLockDuplicatePage** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocLockDuplicatePage** <br/> |
   

