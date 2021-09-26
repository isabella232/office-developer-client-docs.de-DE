---
title: Zelle "A" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
ms.localizationpriority: medium
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: 260c9cb9a6bc5b538857585208ba9b8d719f07ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608767"
---
# <a name="a-cell-geometry-section"></a>Zelle "A" (Abschnitt "Geometry")

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|Zeile|Beschreibung|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Der Abstand vom Mittelpunkt des Bogens bis zum Mittelpunkt seiner Sehne.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die  X-Koordinate des Kontrollpunkts des Bogens, ein Punkt auf dem Bogen. Der Kontrollpunkt befindet sich am besten etwa in der Mitte zwischen den Anfangs- und Endscheitelpunkten des Bogens. Andernfalls kann der Bogen zu einer extrem großen Größe werden, um den Kontrollpunkt zu durchlaufen, was zu unvorhersehbaren Ergebnissen führt.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die Polylinienformel.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Der vorletzte Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der zweite Knoten des Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine  X-Koordinate eines Punkts auf der unendlichen Linie; gepaart mit einer y-Koordinate, dargestellt durch die Zelle [B.](b-cell-geometry-section.md)   <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine  X-Koordinate eines Punkts auf der Ellipse; gepaart mit einer y-Koordinate, dargestellt durch die Zelle [B.](b-cell-geometry-section.md)   <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie zum Abrufen eines Verweises auf die Zelle A anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . A  *j*            where  *i*  and  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . A1 (InfiniteLine- und Ellipse-Zeilen), wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle A anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j* where *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine- und Ellipse-Zeilen)  <br/> |
| Zellenindex:  <br/> |**visBow** (ArcTo-Zeile)  <br/> |
||**visControlX** (Zeile "EllipticalArcTo")  <br/> |
||**visControlY** (Zeile "EllipticalArcTo")  <br/> |
||**visPolylineData** (Polylinezeile)  <br/> |
||**visNURBSKnot** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot** (SplineStart- und SplineKnot-Zeilen)  <br/> |
||**visInfiniteLineX2** (Zeile "InfiniteLine")  <br/> |
||**visEllipseMajorX** (Zeile "Ellipse")  <br/> |
   

