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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301484"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>Zelle "PageShapeSplit" (Abschnitt "Page Layout")

Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Automatische Shape-Teilung nicht zulassen.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Automatische Shape-Teilung zulassen (Standardeinstellung).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. Die Standardeinstellungen für Shapes hängen vom Typ der Zeichnung ab. 
  
Um die Aufteilung auf Anwendungsebene zu aktivieren oder zu deaktivieren, verwenden Sie die Einstellung **Verbindungs Aufteilung aktivieren** auf der Registerkarte **erweitert** des Dialogfelds **Visio-Optionen** (Klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf der **Visio** -Seite auf **Optionen** . , und klicken Sie dann auf **erweitert** ). 
  
Informationen zum Aktivieren oder Deaktivieren der Aufteilung auf Shape-Ebene finden Sie in den Zellen ShapeSplit und ShapeSplittable. 
  
Wenn Sie einen Verweis auf die Zelle PageShapeSplit aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageShapeSplit  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PageShapeSplit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOSplit** <br/> |
   

