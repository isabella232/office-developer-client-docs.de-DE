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
ms.openlocfilehash: 42f346b06cad827cfe56fc113a8387d1a31a6867
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341587"
---
# <a name="a-cell-geometry-section"></a>Zelle "A" (Abschnitt "Geometry")

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|**Zeile**|**Beschreibung**|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Der Abstand vom Mittelpunkt des Bogens bis zum Mittelpunkt seiner Sehne.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *x* -Koordinate des Kontrollpunkts des Bogens, ein Punkt auf dem Bogen. Der Steuerpunkt befindet sich am besten in der Mitte zwischen dem Anfangs-und Endscheitel des Bogens. Andernfalls kann der Bogen zu einer extremen Größe anwachsen, um den Kontrollpunkt mit unvorhersehbaren Ergebnissen zu durchlaufen.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die Polylinienformel.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Der vorletzte Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Der zweite Knoten des Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *x* -Koordinate eines Punkts auf der unendlichen Reihe; gepaart mit der *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *x* -Koordinate eines Punkts auf der Ellipse; gepaart mit der *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle A aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . A *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . A1 (Endpunkte und Ellipse) wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle A aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* = ** 0, 1, 2...  <br/> |
||**visRowVertex** (Zeilen für unendliche und Ellipse)  <br/> |
| Zellenindex:  <br/> |**visBow** (ArcTo-Zeile)  <br/> |
||**visControlX** (EllipticalArcTo-Zeile)  <br/> |
||**visControlY** (EllipticalArcTo-Zeile)  <br/> |
||**visPolylineData** (Polylinie)  <br/> |
||**visNURBSKnot** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot** (Zeile SplineStart-und SplineKnot-Zeilen)  <br/> |
||**visInfiniteLineX2** (Unendliche Zeile)  <br/> |
||**visEllipseMajorX** (Zeile Ellipse)  <br/> |
   

