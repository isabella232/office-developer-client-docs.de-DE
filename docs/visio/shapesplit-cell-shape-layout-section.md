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
ms.openlocfilehash: b782977bd5b7e828223675eb16f4e7e48f4ca55d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798051"
---
# <a name="shapesplit-cell-shape-layout-section"></a>ShapeSplit Cell (Shape Layout Section)

Gibt an, ob dieses Shape andere Shapes teilen kann, sofern diese teilbar sind.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Teilen anderer Shapes durch dieses Shape nicht zulassen.  <br/> |**visSLOSplitNone** <br/> |
| 1  <br/> | Teilen anderer Shapes durch dieses Shape zulassen.  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Shape, das andere Shapes teilen kann, muss entweder ein 2D-Shape oder ein platzierbares 1D-Shape sein. 
  
Das automatische Teilen von Shapes wird auf drei unterschiedlichen Ebenen aktiviert und deaktiviert: Anwendung, Zeichenblatt und Shape. In der Standardeinstellung ist das Teilen auf den Ebenen Anwendung und Zeichenblatt aktiviert, bei Shapes hängt es vom Zeichnungstyp ab. 
  
Zum Aktivieren oder Deaktivieren des Teilens auf Anwendungsebene, verwenden Sie die Einstellung **Connector aufteilen aktivieren** auf der Registerkarte **Erweitert** im Dialogfeld **Visio-Optionen** (klicken Sie auf der Registerkarte **Datei** , klicken Sie auf **Optionen**, und klicken Sie dann auf ** Erweiterte**). 
  
Lesen Sie zum Aktivieren oder Deaktivieren des Teilens auf einem Zeichenblatt die Informationen zur Zelle PageShapeSplit. 
  
Wenn Sie ein 1D-Shape teilbar machen möchten, lesen Sie die Informationen zur Zelle ShapeSplittable.
  
Zum Abrufen eines Verweises auf die Zelle ShapeSplit nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeSplit  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapeSplit aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOSplit** <br/> |
   

