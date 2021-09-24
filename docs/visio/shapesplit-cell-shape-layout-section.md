---
title: Zelle "ShapeSplit" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
ms.localizationpriority: medium
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Gibt an, ob dieses Shape andere Shapes teilen kann, sofern diese teilbar sind.
ms.openlocfilehash: da89333e8a190d2ad573b1d088480c5e0df6efd8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549609"
---
# <a name="shapesplit-cell-shape-layout-section"></a>Zelle "ShapeSplit" (Abschnitt "Shape Layout")

Gibt an, ob dieses Shape andere Shapes teilen kann, sofern diese teilbar sind.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Teilen anderer Shapes durch dieses Shape nicht zulassen.  <br/> |**visSLOSplitNone** <br/> |
| 1  <br/> | Teilen anderer Shapes durch dieses Shape zulassen.  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein Shape, das andere Shapes teilen kann, muss entweder ein 2D-Shape oder ein platzierbares 1D-Shape sein. 
  
Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert, bei Shapes hängt es vom Zeichnungstyp ab. 
  
Um das Teilen auf Anwendungsebene zu aktivieren oder zu deaktivieren, verwenden **Sie** die Einstellung zum Teilen des Connectors auf der Registerkarte **"Erweitert"** des Dialogfelds **"Visio Optionen"** (klicken Sie auf die Registerkarte **"Datei",** klicken Sie auf **"Optionen"** und dann auf **"Erweitert").** 
  
Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle PageShapeSplit. 
  
Wenn Sie ein 1D-Shape teilbar machen möchten, lesen Sie die Informationen zur Zelle ShapeSplittable.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle ShapeSplit anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeSplit  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeSplit anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOSplit** <br/> |
   

