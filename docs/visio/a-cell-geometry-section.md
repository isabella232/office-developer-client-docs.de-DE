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
  
|Row|Beschreibung|
|:-----|:-----|
|[ArcTo](arcto-row-geometry-section.md) <br/> | Der Abstand vom Mittelpunkt des Bogens bis zum Mittelpunkt seiner Sehne.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *x* -Koordinate des Kontrollpunktes des Bogens, ein Punkte auf dem Bogen. Der Steuerpunkt befindet sich am besten ungefähr auf halbem Weg zwischen dem Anfangs-und Endpunkt des Bogens. Andernfalls kann der Bogen in eine extreme Größe vergrößert werden, um den Kontrollpunkte mit unvorhersehbaren Ergebnissen zu passieren.  <br/> |
|[PolyLineTo](polylineto-row-geometry-section.md) <br/> | Die Polylinienformel.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Der vorletzte Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Der zweite Knoten des Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).  <br/> |
|[Zeile InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *x* -Koordinate eines Points auf der unendlichen Leine; gepaart mit der *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *x* -Koordinate eines Kommas auf der Ellipse; gepaart mit der *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf eine Zelle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . A *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . A1 (endlos-und Ellipsen Zeilen) wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf eine Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* , wobei *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Endlos-und Ellipsen Zeilen)  <br/> |
| Zellenindex:  <br/> |**visBow** (ArcTo-Zeile)  <br/> |
||**visControlX** (EllipticalArcTo-Zeile)  <br/> |
||**visControlY** (EllipticalArcTo-Zeile)  <br/> |
||**visPolylineData** (Polylinie Zeile)  <br/> |
||**visNURBSKnot** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot** (Zeile SplineStart-und SplineKnot-Zeilen)  <br/> |
||**visInfiniteLineX2** (Endlos Zeile)  <br/> |
||**visEllipseMajorX** (Ellipsen Zeile)  <br/> |
   

