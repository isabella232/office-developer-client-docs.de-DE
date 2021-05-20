---
title: Zelle "ShapeSplittable" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
localization_priority: Normal
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Zeigt an, ob dieses 1D-Shape geteilt werden kann.
ms.openlocfilehash: 9f92cf7d147be8e59d860bcc8a958bf0cdc008c6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427073"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>Zelle "ShapeSplittable" (Abschnitt "Shape Layout")

Zeigt an, ob dieses 1D-Shape geteilt werden kann. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Teilen des Shapes nicht zulassen.  <br/> |**visSLOSplittableNone** <br/> |
| 1  <br/> | Teilen des Shapes zulassen.  <br/> |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>Hinweise

Das Standardverhalten von Verbindern und anderen 1D-Shapes hängt vom Zeichnungstyp ab. 
  
Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. 
  
Verwenden Sie zum Aktivieren oder Deaktivieren der  Aufteilung auf Anwendungsebene  die Einstellung Connectorteilung aktivieren auf der  Registerkarte Erweitert im Dialogfeld **Visio-Optionen** (klicken Sie auf die Registerkarte Datei, klicken Sie auf **Optionen** und dann auf **Erweitert** ). 
  
Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle [PageShapeSplit](pageshapesplit-cell-page-layout-section.md). 
  
Wenn Sie ein Shape so konfigurieren möchten, dass es teilbare 1D-Shapes teilt, lesen Sie die Informationen zur Zelle [ShapeSplit](shapesplit-cell-shape-layout-section.md). 
  
Verwenden Sie zum Erhalten eines Verweises auf die Zelle ShapeSplittable anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeSplittable  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapeSplittable nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOSplittable** <br/> |
   

