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
ms.openlocfilehash: e2db881465a19b34d5788f1621f15c4d7d15c293
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798058"
---
# <a name="shapesplittable-cell-shape-layout-section"></a>ShapeSplittable Cell (Shape Layout Section)

Zeigt an, ob dieses 1D-Shape geteilt werden kann. 
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Teilen des Shapes nicht zulassen.  <br/> |**visSLOSplittableNone** <br/> |
| 1  <br/> | Teilen des Shapes zulassen.  <br/> |**visSLOSplittableAllow** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Standardverhalten von Verbindern und anderen 1D-Shapes hängt vom Zeichnungstyp ab. 
  
Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. 
  
Zum Aktivieren oder Deaktivieren des Teilens auf Anwendungsebene, verwenden Sie die Einstellung **Connector aufteilen aktivieren** auf der Registerkarte **Erweitert** im Dialogfeld **Visio-Optionen** (klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Optionen**, und klicken Sie dann auf ** Erweiterte** ). 
  
Zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt finden die Informationen zur Zelle [PageShapeSplit](pageshapesplit-cell-page-layout-section.md) . 
  
Wenn ein Shape teilbare 1D-Shapes können, lesen Sie die Zelle [ShapeSplit](shapesplit-cell-shape-layout-section.md) . 
  
Zum Abrufen eines Verweises auf die Zelle ShapeSplittable nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeSplittable  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapeSplittable aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOSplittable** <br/> |
   

