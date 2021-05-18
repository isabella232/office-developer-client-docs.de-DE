---
title: Zelle "PageShapeSplit" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422019"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>Zelle "PageShapeSplit" (Abschnitt "Page Layout")

Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Automatische Shape-Teilung nicht zulassen.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Automatische Shape-Teilung zulassen (Standardeinstellung).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Hinweise

Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. Die Standardeinstellungen für Shapes hängen vom Typ der Zeichnung ab. 
  
Verwenden Sie zum Aktivieren oder Deaktivieren der  Aufteilung auf Anwendungsebene  die Einstellung Connectorteilung aktivieren auf der Registerkarte Erweitert im Dialogfeld  **Visio-Optionen** (klicken Sie auf die Schaltfläche **Office,** klicken Sie auf der Registerkarte **Visio** auf Optionen, und klicken Sie dann auf **Erweitert** ). 
  
Informationen zum Aktivieren oder Deaktivieren der Aufteilung auf Formebene finden Sie in den Zellen ShapeSplit und ShapeSplittable. 
  
Um einen Verweis auf die Zelle PageShapeSplit anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageShapeSplit  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle PageShapeSplit nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOSplit** <br/> |
   

