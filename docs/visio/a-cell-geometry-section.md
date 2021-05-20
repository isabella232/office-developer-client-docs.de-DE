---
title: Zelle "A" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541302"
---
# <a name="a-cell-geometry-section"></a>Zelle "A" (Abschnitt "Geometry")

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|Zeile|Beschreibung|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Der Abstand vom Mittelpunkt des Bogens bis zum Mittelpunkt seiner Sehne.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die  x-Koordinate des Kontrollpunkts des Bogens, ein Punkt im Bogen. Der Kontrollpunkt befindet sich am besten ungefähr auf halbem Weg zwischen den Scheitelpunkte am Anfang und Ende des Bogens. Andernfalls kann der Bogen zu einer extremen Größe anwachsen, um den Kontrollpunkt mit unvorhersehbaren Ergebnissen zu passieren.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die Polylinienformel.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Der vorletzte Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der zweite Knoten des Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine  x-Koordinate eines Punkts auf der unendlichen Linie; gekoppelt mit *y* -koordinate, die durch die [Zelle B dargestellt](b-cell-geometry-section.md) wird.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine  x-Koordinate eines Punkts auf der Ellipse; gekoppelt mit *y* -koordinate, die durch die [Zelle B dargestellt](b-cell-geometry-section.md) wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle A anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . A  *j*            where  *i*  and  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . A1 (InfiniteLine- und Ellipsenzeilen),  *wobei i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle A nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine- und Ellipsenzeilen)  <br/> |
| Zellenindex:  <br/> |**visBow** (ArcTo-Zeile)  <br/> |
||**visControlX** (EllipticalArcTo-Zeile)  <br/> |
||**visControlY** (EllipticalArcTo-Zeile)  <br/> |
||**visPolylineData** (Polyline-Zeile)  <br/> |
||**visNURBSKnot** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot** (SplineStart- und SplineKnot-Zeilen)  <br/> |
||**visInfiniteLineX2** (InfiniteLine-Zeile)  <br/> |
||**visEllipseMajorX** (Ellipsenzeile)  <br/> |
   

