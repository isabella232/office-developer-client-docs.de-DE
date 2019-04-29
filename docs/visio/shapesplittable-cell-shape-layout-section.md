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
   
## <a name="remarks"></a>Bemerkungen

Das Standardverhalten von Verbindern und anderen 1D-Shapes hängt vom Zeichnungstyp ab. 
  
Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. 
  
Um die Aufteilung auf Anwendungsebene zu aktivieren oder zu deaktivieren, verwenden Sie die Einstellung **Verbinder-Aufteilung aktivieren** auf der Registerkarte **erweitert** des Dialogfelds **Visio-Optionen** (Klicken Sie auf die Registerkarte **Datei** , dann auf **Optionen**und dann auf ** Advanced** ). 
  
Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle [PageShapeSplit](pageshapesplit-cell-page-layout-section.md). 
  
Wenn Sie ein Shape so konfigurieren möchten, dass es teilbare 1D-Shapes teilt, lesen Sie die Informationen zur Zelle [ShapeSplit](shapesplit-cell-shape-layout-section.md). 
  
Wenn Sie einen Verweis auf die Zelle ShapeSplittable aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeSplittable  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapeSplittable aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOSplittable** <br/> |
   

