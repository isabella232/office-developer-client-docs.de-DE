---
title: Zelle "LockPreview" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Legt fest, ob jedes Mal, wenn Sie eine Zeichnung speichern, eine Vorschau gespeichert wird.
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418862"
---
# <a name="lockpreview-cell-document-properties-section"></a>Zelle "LockPreview" (Abschnitt "Document Properties")

Legt fest, ob jedes Mal, wenn Sie eine Zeichnung speichern, eine Vorschau gespeichert wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Vorschau nicht jedes Mal speichern, wenn eine Zeichnung gespeichert wird.  <br/> |
| FALSE  <br/> | Vorschau jedes Mal speichern, wenn eine Zeichnung gespeichert wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle LockPreview anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockPreview  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockPreview nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocLockPreview** <br/> |
   

