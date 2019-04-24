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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356112"
---
# <a name="previewscope-cell-document-properties-section"></a>Zelle "PreviewScope" (Abschnitt "Document Properties")

Legt fest, ob die Zeichnung eine Vorschau mit einschließt. Wenn die Zeichnung eine Vorschau mit einschließt, wird hier definiert, ob die Vorschau nur die erste Seite oder alle Seiten der Zeichnung zeigt.
  
|**Wert**|**Umfang der Vorschau**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Erste Seite  <br/> |**visDocPreviewScope1stPage** <br/> |
| 1  <br/> | Keine  <br/> |**visDocPreviewScopeNone** <br/> |
| 2  <br/> | Alle Seiten  <br/> |**visDocPreviewScopeAllPages** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Eigenschaften** auf der Registerkarte **Zusammenfassung** festlegen (Klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf die Registerkarte **Info** , klicken Sie auf **Dokumenteigenschaften**und dann auf **Erweiterte Eigenschaften**).
  
Wenn Sie einen Verweis auf die Zelle "PreviewScope aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | "PreviewScope  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "PreviewScope aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowDoc** <br/> |
| Zellenindex:  <br/> |**visDocPreviewScope** <br/> |
   

