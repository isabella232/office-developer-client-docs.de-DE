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
| 1  <br/> | Detaillierte  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Eigenschaften** auf der Registerkarte **Zusammenfassung** festlegen (Klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf die Registerkarte **Info** , klicken Sie auf **Dokumenteigenschaften**und dann auf **Erweiterte Eigenschaften**).
  
Wenn Sie einen Verweis auf die Zelle "PreviewQuality aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "PreviewQuality  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "PreviewQuality aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocPreviewQuality** <br/> |
   

