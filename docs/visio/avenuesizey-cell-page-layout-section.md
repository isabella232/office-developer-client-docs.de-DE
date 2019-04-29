---
title: Zelle "AvenueSizeY" (Abschnitt "Page Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm70
localization_priority: Normal
ms.assetid: 9ff2893c-afe5-505e-0b55-48ec1de08a5f
description: Bestimmt den vertikalen Abstand zwischen den Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds Layout konfigurieren (Klicken Sie auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu Layout und dann auf Weitere Layoutoptionen).
ms.openlocfilehash: 283de8925e34c470fd1f9e78b8ae58882be8b7fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420206"
---
# <a name="avenuesizey-cell-page-layout-section"></a>Zelle "AvenueSizeY" (Abschnitt "Page Layout")

Bestimmt den vertikalen Abstand zwischen den Shapes auf dem Zeichenblatt, wenn Sie Shapes mithilfe des Dialogfelds **Layout konfigurieren** (Klicken Sie auf der Register **Karte Entwurf** in der Gruppe **Layout** auf Seite **neu Layout** ), und klicken Sie dann auf **Weitere Layout-Optionen**).
  
## <a name="remarks"></a>Bemerkungen

Sie können diesen Wert auch im Dialogfeld **Abstände für Layout und Routing** festlegen. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Seite einrichten** auf den Pfeil, wählen Sie die Registerkarte **Layout und Routing** aus, und klicken Sie dann auf **Abstand**.)
  
Das dynamische Raster verwendet die Einstellung in der Zelle Zelle AvenueSizeY, wenn nur eine Form zum Berechnen des vertikalen Abstands zur Verfügung steht. Um das dynamische Raster zu verwenden, wählen Sie auf der Registerkarte **Ansicht** in der Gruppe **visuelle Hilfsmittel** die Option **dynamisches Raster**aus.
  
Wenn Sie einen Verweis auf die Zelle Zelle AvenueSizeY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle AvenueSizeY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle AvenueSizeY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowPageLayout** <br/> |
| Zellenindex:  <br/> |**visPLOAvenueSizeY** <br/> |
   

