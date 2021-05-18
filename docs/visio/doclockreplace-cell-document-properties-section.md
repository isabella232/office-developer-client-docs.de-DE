---
title: Zelle "DocLockReplace" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Bestimmt, ob die Benutzeroberfläche des Ersetzen-Shapes für dieses Dokument deaktiviert werden soll.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413423"
---
# <a name="doclockreplace-cell-document-properties-section"></a>Zelle "DocLockReplace" (Abschnitt "Document Properties")

Bestimmt, ob die Benutzeroberfläche des Ersetzen-Shapes für dieses Dokument deaktiviert werden soll. 
  
|||
|:-----|:-----|
|TRUE  <br/> |Die **Schaltfläche Shape ersetzen** ist in der Benutzeroberfläche ausgegraut.  <br/> |
|FALSE  <br/> |Die **Schaltfläche Shape ersetzen** ist auf der Benutzeroberfläche aktiv. Benutzer können das Feature Shape ersetzen in diesem Dokument verwenden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die **Zelle DocLockReplace** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DocLocReplace  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **DocLocReplace-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocLockReplace ** <br/> |
   

