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
ms.openlocfilehash: b907552c2346292a6b14baf16481b6b40cc80fc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796363"
---
# <a name="a-cell-geometry-section"></a>A Cell (Geometry Section)

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Der Abstand vom Mittelpunkt des Bogens bis zum Mittelpunkt seiner Sehne.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *X* -Koordinate des Kontrollpunkts des Bogens, einen Punkt auf dem Bogen. Kontrollpunkts ist die beste in der Mitte zwischen dem ersten und letzten Scheitelpunkt des Bogens. Andernfalls kann Bogens extrem große anwachsen, um passieren Kontrollpunkts weitergibt.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die Polylinienformel.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Der vorletzte Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der zweite Knoten des Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *X* -Koordinate eines Punkts auf der unendlichen Linie gepaart mit einer *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *X* -Koordinate eines Punkts auf der Ellipse; gepaart mit einer *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Zum Abrufen eines Verweises auf die Zelle A nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft verwenden Sie zu können: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . Ein *j* wobei *i* und *j* = < 1 >, 2, 3...  <br/> |
|| Geometrie *i* . A1 (Zeilen UnendlicheLinie und Ellipse) wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle A aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Zeilen UnendlicheLinie und Ellipse)  <br/> |
| Zellenindex:  <br/> |**visBow** (Zeile ArcTo)  <br/> |
||**visControlX** (Zeile EllipticalArcTo)  <br/> |
||**visControlY** (Zeile EllipticalArcTo)  <br/> |
||**visPolylineData** (Zeile Polyline)  <br/> |
||**visNURBSKnot** (Zeile NURBSTo)  <br/> |
||**visSplineKnot** (Zeilen SplineStart und SplineKnot)  <br/> |
||**visInfiniteLineX2** (Zeile InfiniteLine)  <br/> |
||**visEllipseMinorX** (Ellipsenzeile)  <br/> |
   

