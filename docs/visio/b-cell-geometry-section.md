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
ms.openlocfilehash: 46c8aa418f495905630fed2833d84afc93945346
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537794"
---
# <a name="b-cell-geometry-section"></a>Zelle "B" (Abschnitt "Geometry")

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|Zeile|Beschreibung|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die  y-Koordinate des Kontrollpunkts eines Bogens.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die zuletzt verwendete Linienstärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der erste Knoten eines Splines.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine  y-Koordinate eines Punkts in einer unendlichen Linie; gekoppelt mit *x* -koordinate, die durch die [Zelle A dargestellt](a-cell-geometry-section.md) wird.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine  y-Koordinate eines Punkts auf einer Ellipse; gekoppelt mit *x* -koordinate, die durch die [Zelle A dargestellt](a-cell-geometry-section.md) wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle B anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . B  *j,*            *wobei i*  und  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . B1 (InfiniteLine- und Ellipsenzeilen)  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle B nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine- und Ellipsenzeilen)  <br/> |
| Zellenindex:  <br/> |**visControlX** (EllipticalArcTo-Zeile)  <br/> |
||**visControlY** (EllipticalArcTo-Zeile)  <br/> |
||**visNURBSWeight** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot2** (SplineStart-Zeile)  <br/> |
||**visInfiniteLineY2** (InfiniteLine-Zeile)  <br/> |
||**visEllipseMajorY** (Ellipsenzeile)  <br/> |
   

