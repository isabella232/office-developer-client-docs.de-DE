---
title: DocLockDuplicatePage Cell (Document Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Bestimmt, ob Seiten im Dokument als boolescher Wert dupliziert werden können.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439660"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>DocLockDuplicatePage Cell (Document Properties section)

Bestimmt, ob Seiten im Dokument als boolescher Wert dupliziert werden können.
  
|||
|:-----|:-----|
|TRUE  <br/> |**Duplikate** im Kontextmenü der Seite und die **Page. Duplicate** -Automatisierungsmethode sind beide deaktiviert.  <br/> |
|FALSE  <br/> |Die Seite kann dupliziert werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **DocLockDuplicatePage** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DocLockDuplicatePage  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **DocLockDuplicatePage** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocLockDuplicatePage** <br/> |
   

