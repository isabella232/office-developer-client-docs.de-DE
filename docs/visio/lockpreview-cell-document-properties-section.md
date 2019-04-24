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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348328"
---
# <a name="lockpreview-cell-document-properties-section"></a>Zelle "LockPreview" (Abschnitt "Document Properties")

Legt fest, ob jedes Mal, wenn Sie eine Zeichnung speichern, eine Vorschau gespeichert wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Vorschau nicht jedes Mal speichern, wenn eine Zeichnung gespeichert wird.  <br/> |
| FALSE  <br/> | Vorschau jedes Mal speichern, wenn eine Zeichnung gespeichert wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle "LockPreview aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "LockPreview  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "LockPreview aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocLockPreview** <br/> |
   

