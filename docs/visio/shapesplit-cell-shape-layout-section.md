---
title: Zelle "ShapeSplit" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
localization_priority: Normal
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: Gibt an, ob dieses Shape andere Shapes teilen kann, sofern diese teilbar sind.
ms.openlocfilehash: 46b42e9be070b54095d3e9a5c247d63be6348f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423559"
---
# <a name="shapesplit-cell-shape-layout-section"></a>Zelle "ShapeSplit" (Abschnitt "Shape Layout")

Gibt an, ob dieses Shape andere Shapes teilen kann, sofern diese teilbar sind.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Teilen anderer Shapes durch dieses Shape nicht zulassen.  <br/> |**visSLOSplitNone** <br/> |
| 1  <br/> | Teilen anderer Shapes durch dieses Shape zulassen.  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Shape, das andere Shapes teilen kann, muss entweder ein 2D-Shape oder ein platzierbares 1D-Shape sein. 
  
Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert, bei Shapes hängt es vom Zeichnungstyp ab. 
  
Verwenden Sie zum Aktivieren oder Deaktivieren der  Aufteilung auf Anwendungsebene  die Einstellung Connectorteilung aktivieren auf der  Registerkarte Erweitert im Dialogfeld **Visio-Optionen** (klicken Sie auf die Registerkarte Datei, klicken Sie auf **Optionen** und dann auf **Erweitert**). 
  
Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle PageShapeSplit. 
  
Wenn Sie ein 1D-Shape teilbar machen möchten, lesen Sie die Informationen zur Zelle ShapeSplittable.
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ShapeSplit anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeSplit  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeSplit nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOSplit** <br/> |
   

