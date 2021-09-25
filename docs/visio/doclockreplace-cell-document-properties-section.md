---
title: Zelle "DocLockReplace" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Bestimmt, ob die Benutzeroberfläche des Ersetzungs-Shapes für dieses Dokument deaktiviert werden soll.
ms.openlocfilehash: 24e2600eeef405ca45922fc276649aedfab5b656
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628444"
---
# <a name="doclockreplace-cell-document-properties-section"></a>Zelle "DocLockReplace" (Abschnitt "Document Properties")

Bestimmt, ob die Benutzeroberfläche des Ersetzungs-Shapes für dieses Dokument deaktiviert werden soll. 
  
|||
|:-----|:-----|
|TRUE  <br/> |Die Schaltfläche **"Shape ersetzen"** ist auf der Benutzeroberfläche ausgegraut.  <br/> |
|FALSE  <br/> |Die Schaltfläche **"Shape ersetzen"** ist auf der Benutzeroberfläche aktiv. Benutzer können das Feature "Shape ersetzen" in diesem Dokument verwenden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die **Zelle DocLockReplace** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DocLocReplace  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **DocLocReplace** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocLockReplace ** <br/> |
   

