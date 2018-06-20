---
title: DocLockReplace Cell (Document Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Bestimmt, ob die Form ersetzen Benutzeroberfläche für dieses Dokument deaktiviert werden soll.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796894"
---
# <a name="doclockreplace-cell-document-properties-section"></a>DocLockReplace Cell (Document Properties Section)

Bestimmt, ob die Form ersetzen Benutzeroberfläche für dieses Dokument deaktiviert werden soll. 
  
|||
|:-----|:-----|
|TRUE  <br/> |Die **Form ersetzen** -Schaltfläche ist nicht in der Benutzeroberfläche verfügbar.  <br/> |
|FALSE  <br/> |Die **Form ersetzen** -Schaltfläche ist aktiv in der Benutzeroberfläche. Benutzer können das Feature Shapes ersetzen Sie in diesem Dokument verwenden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **DocLockReplace** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DocLocReplace  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **DocLocReplace** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |** VisDocLockReplace ** <br/> |
   

