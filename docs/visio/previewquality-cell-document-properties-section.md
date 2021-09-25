---
title: Zelle "PreviewQuality" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
ms.localizationpriority: medium
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Bestimmt, ob die Zeichnungsvorschau Entwurfsqualität hat oder detailgetreu sein soll.
ms.openlocfilehash: 39aed22a6a489116aab46f9f6ec558775b420961
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573726"
---
# <a name="previewquality-cell-document-properties-section"></a>Zelle "PreviewQuality" (Abschnitt "Document Properties")

Bestimmt, ob die Zeichnungsvorschau Entwurfsqualität hat oder detailgetreu sein soll.
  
|**Wert**|**PreviewQuality**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Entwurf  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Detaillierte  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Sie können diesen Wert auch auf der Registerkarte **"Zusammenfassung"** im Dialogfeld **"Eigenschaften"** festlegen (klicken Sie auf die Schaltfläche **Office,** klicken Sie auf die Registerkarte **"Info",** klicken Sie auf **"Dokumenteigenschaften"** und dann auf **"Erweiterte Eigenschaften").**
  
Um einen Verweis auf die Zelle "PreviewQuality" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PreviewQuality  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "PreviewQuality" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocPreviewQuality** <br/> |
   

