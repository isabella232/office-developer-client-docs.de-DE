---
title: Zelle "PreviewScope" (Abschnitt "Document Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm820
localization_priority: Normal
ms.assetid: d03ae1b3-da6c-56d3-4f96-6e131c04e93e
description: Legt fest, ob die Zeichnung eine Vorschau mit einschließt. Wenn die Zeichnung eine Vorschau mit einschließt, wird hier definiert, ob die Vorschau nur die erste Seite oder alle Seiten der Zeichnung zeigt.
ms.openlocfilehash: 34dbc9ac02032b2cb5cb6373c3c6361e3d822312
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426506"
---
# <a name="previewscope-cell-document-properties-section"></a>Zelle "PreviewScope" (Abschnitt "Document Properties")

Legt fest, ob die Zeichnung eine Vorschau mit einschließt. Wenn die Zeichnung eine Vorschau mit einschließt, wird hier definiert, ob die Vorschau nur die erste Seite oder alle Seiten der Zeichnung zeigt.
  
|**Wert**|**Umfang der Vorschau**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Erste Seite  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1  <br/> | Keinen  <br/> |**visDocPreviewScopeNone** <br/> |
| 2  <br/> | Alle Seiten  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Hinweise

Sie können diesen Wert  auch auf  der Registerkarte Zusammenfassung im Dialogfeld Eigenschaften festlegen (klicken Sie auf die Schaltfläche **Office,** klicken Sie auf die Registerkarte **Info,** klicken Sie auf Dokumenteigenschaften **und** dann auf **Erweiterte Eigenschaften**).
  
Um einen Verweis auf die Zelle PreviewScope anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PreviewScope  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PreviewScope nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocPreviewScope** <br/> |
   

