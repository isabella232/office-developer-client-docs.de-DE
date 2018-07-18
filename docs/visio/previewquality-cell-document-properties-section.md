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
ms.openlocfilehash: bc8a53934b6dad06a0867cc73cdfacfa02d2b438
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797707"
---
# <a name="previewquality-cell-document-properties-section"></a>PreviewQuality Cell (Document Properties Section)

Bestimmt, ob die Zeichnungsvorschau Entwurfsqualität hat oder detailgetreu sein soll.
  
|**Wert**|**PreviewQuality**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Entwurf  <br/> |**visDocPreviewQualityDraft** <br/> |
| 1  <br/> | Detailliert  <br/> |**visDocPreviewQualityDetailed** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch auf der Registerkarte **Zusammenfassung** im Dialogfeld **Eigenschaften** festlegen (klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf der Registerkarte **Info** , klicken Sie auf **Dokumenteigenschaften**, und klicken Sie dann auf **Erweiterte Eigenschaften**).
  
Wenn Sie einen Verweis auf die Zelle PreviewQuality aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PreviewQuality  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PreviewQuality aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocPreviewQuality** <br/> |
   

