---
title: Zelle "B" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796421"
---
# <a name="b-cell-geometry-section"></a>B Cell (Geometry Section)

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Kontrollpunkts des Bogens.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die zuletzt verwendete Linienstärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der erste Knoten eines Splines.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *y* -Koordinate eines Punkts auf der unendlichen Linie; gepaart mit einer *X* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *y* -Koordinate eines Punkts auf der Ellipse; gepaart mit einer *X* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Referenz auf die Zelle B nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . B *j* wobei *i* und *j* = < 1 >, 2, 3...  <br/> |
|| Geometrie *i* . B1 (Zeilen UnendlicheLinie und Ellipse)  <br/> |
   
Wenn Sie eine Referenz auf die Zelle B aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...  <br/> |
||visRowVertex (Zeilen InfiniteLine und Ellipse)  <br/> |
| Zellenindex:  <br/> |visControlX (Zeile EllipticalArcTo)  <br/> |
||visControlY (Zeile EllipticalArcTo)  <br/> |
||visNURBSWeight (Zeile NURBSTo)  <br/> |
||visSplineKnot2 (Zeile SplineStart)  <br/> |
||visInfiniteLineY2 (Zeile InfiniteLine)  <br/> |
||visEllipseMajorY (Zeile Ellipse)  <br/> |
   

