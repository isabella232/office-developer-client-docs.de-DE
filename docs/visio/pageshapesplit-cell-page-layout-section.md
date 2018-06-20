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
ms.openlocfilehash: 7f1df0158cde6853c5518597c853cb56151eefbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797599"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>PageShapeSplit Cell (Page Layout Section)

Gibt an, ob Shapes auf dem Zeichenblatt automatisch geteilt werden können.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Automatische Shape-Teilung nicht zulassen.  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |Automatische Shape-Teilung zulassen (Standardeinstellung).  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert. Die Standardeinstellungen für Shapes hängen vom Typ der Zeichnung ab. 
  
Zum Aktivieren oder Deaktivieren des Teilens auf Anwendungsebene, verwenden Sie die Einstellung **Connector aufteilen aktivieren** auf der Registerkarte **Erweitert** im Dialogfeld **Visio-Optionen** (klicken Sie auf die **Office** -Schaltfläche, klicken Sie auf der **Visio** - **Optionen** Registerkarte, und klicken Sie dann auf **Erweitert** ). 
  
Zum Aktivieren oder Deaktivieren des Teilens auf Shape-Ebene, finden Sie in den Zellen ShapeSplit und ShapeSplittable. 
  
Wenn Sie einen Verweis auf die Zelle PageShapeSplit nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |PageShapeSplit  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PageShapeSplit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
|Zellenindex:  <br/> |**visPLOSplit** <br/> |
   

