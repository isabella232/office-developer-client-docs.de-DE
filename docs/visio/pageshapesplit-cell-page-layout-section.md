---
title: Zelle "PageShapeSplit" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
ms.localizationpriority: medium
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.
ms.openlocfilehash: d8e50a67746135ca43c3a9bee337be2fae31c827
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623236"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>Zelle "PageShapeSplit" (Abschnitt "Page Layout")

Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Automatische Shape-Teilung nicht zulassen.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Automatische Shape-Teilung zulassen (Standardeinstellung).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. Die Standardeinstellungen für Shapes hängen vom Typ der Zeichnung ab. 
  
Um das Teilen auf Anwendungsebene zu aktivieren oder zu deaktivieren, verwenden Sie die Einstellung **"Verbinderteilung aktivieren"** auf der Registerkarte **"Erweitert"** des Dialogfelds **"Visio Optionen"** (klicken Sie auf die Schaltfläche **Office,** klicken Sie auf der Registerkarte **Visio** auf **Optionen,** und klicken Sie dann auf **"Erweitert").** 
  
Informationen zum Aktivieren oder Deaktivieren der Teilung auf Shape-Ebene finden Sie in den Zellen "ShapeSplit" und "ShapeSplittable". 
  
Um einen Verweis auf die Zelle "PageShapeSplit" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageShapeSplit  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PageShapeSplit anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOSplit** <br/> |
   

