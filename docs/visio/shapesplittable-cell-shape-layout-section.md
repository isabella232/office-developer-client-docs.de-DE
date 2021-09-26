---
title: Zelle "ShapeSplittable" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60081
ms.localizationpriority: medium
ms.assetid: 6330304a-71f3-62b4-1b27-14495e3f12c3
description: Zeigt an, ob dieses 1D-Shape geteilt werden kann.
ms.openlocfilehash: 31a64e466846b9d050c4993c26241933f96868d1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627443"
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
  
Um das Teilen auf Anwendungsebene zu aktivieren oder zu deaktivieren, verwenden **Sie** die Einstellung zum Teilen des Connectors auf der Registerkarte **"Erweitert"** des Dialogfelds **"Visio Optionen"** (klicken Sie auf die Registerkarte **"Datei",** klicken Sie auf **"Optionen"** und dann auf **"Erweitert").** 
  
Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle [PageShapeSplit](pageshapesplit-cell-page-layout-section.md). 
  
Wenn Sie ein Shape so konfigurieren möchten, dass es teilbare 1D-Shapes teilt, lesen Sie die Informationen zur Zelle [ShapeSplit](shapesplit-cell-shape-layout-section.md). 
  
Verwenden Sie zum Abrufen eines Verweises auf die ShapeSplittable-Zelle anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeSplittable  <br/> |
   
Verwenden Sie zum Abrufen eines Verweises auf die Zelle ShapeSplittable anhand des Indexes eines Programms die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOSplittable** <br/> |
   

