---
title: Zelle "PreviewQuality" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm815
localization_priority: Normal
ms.assetid: b7d90666-a1bb-f0de-32da-b2855977f648
description: Bestimmt, ob die Zeichnungsvorschau Entwurfsqualität hat oder detailgetreu sein soll.
ms.openlocfilehash: 9db2d3e1eb829bfd2ad787fcfc94cd9ba5abaf9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416818"
---
# <a name="previewquality-cell-document-properties-section"></a>Zelle "PreviewQuality" (Abschnitt "Document Properties")

Bestimmt, ob die Zeichnungsvorschau Entwurfsqualität hat oder detailgetreu sein soll.
  
|**Wert**|**PreviewQuality**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Entwurf  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Detailliert  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert  auch auf  der Registerkarte Zusammenfassung im Dialogfeld Eigenschaften festlegen (klicken Sie auf die Schaltfläche **Office,** klicken Sie auf die Registerkarte **Info,** klicken Sie auf Dokumenteigenschaften **und** dann auf **Erweiterte Eigenschaften**).
  
Um einen Verweis auf die Zelle PreviewQuality anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PreviewQuality  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PreviewQuality nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocPreviewQuality** <br/> |
   

