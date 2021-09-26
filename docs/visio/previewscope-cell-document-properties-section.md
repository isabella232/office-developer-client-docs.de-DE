---
title: Zelle "PreviewScope" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
ms.localizationpriority: medium
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Legt fest, ob die Zeichnung eine Vorschau mit einschließt. Wenn die Zeichnung eine Vorschau mit einschließt, wird hier definiert, ob die Vorschau nur die erste Seite oder alle Seiten der Zeichnung zeigt.
ms.openlocfilehash: 58b9ac70a853dbf7dccbdf723738b0aeb00608d2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627688"
---
# <a name="previewscope-cell-document-properties-section"></a>Zelle "PreviewScope" (Abschnitt "Document Properties")

Legt fest, ob die Zeichnung eine Vorschau mit einschließt. Wenn die Zeichnung eine Vorschau mit einschließt, wird hier definiert, ob die Vorschau nur die erste Seite oder alle Seiten der Zeichnung zeigt.
  
|**Wert**|**Umfang der Vorschau**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Erste Seite  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1  <br/> | Keinen  <br/> |**visDocPreviewScopeNone** <br/> |
| 2  <br/> | Alle Seiten  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch auf der Registerkarte **"Zusammenfassung"** im Dialogfeld **"Eigenschaften"** festlegen (klicken Sie auf die Schaltfläche **Office,** klicken Sie auf die Registerkarte **"Info",** klicken Sie auf **"Dokumenteigenschaften"** und dann auf **"Erweiterte Eigenschaften").**
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "PreviewScope" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PreviewScope  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PreviewScope anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocPreviewScope** <br/> |
   

