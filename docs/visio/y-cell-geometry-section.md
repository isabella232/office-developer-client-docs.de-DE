---
title: Zelle "Y" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Stellt eine y-Koordinate in einer Form in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 7dea96b544c84f09abe1d72304da0bacaa09432f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540490"
---
# <a name="y-cell-geometry-section"></a>Zelle "Y" (Abschnitt "Geometrie")

Stellt  eine y-Koordinate in einer Form in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet. 
  
|Zeile|Beschreibung|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Wenn die MoveTo-Zeile die erste Zeile im Abschnitt  ist, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts eines Pfads dar. Wenn die MoveTo-Zeile zwischen zwei Zeilen angezeigt  wird, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Die  y-Koordinate des endenden Scheitelpunkts eines geraden Abschnitts.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die  y-Koordinate des endenden Scheitelpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die  y-Koordinate des endenden Scheitelpunkts eines elliptischen Bogens.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die  y-Koordinate des endenden Scheitelpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die  y-Koordinate des letzten Kontrollpunkts eines nicht einheitlich rationalen B-Splines (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Die  y-Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die  y-Koordinate eines Kontrollpunkts.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine  *y-Koordinate*  eines Punkts auf der unendlichen Linie.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die  y-Koordinate der Mitte der Ellipse.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle Y anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . Y  *j,*            *wobei i*  und  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . Y1 (InfiniteLine- und Ellipsenzeilen), wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine- und Ellipsenzeilen)  <br/> |
| Zellenindex:  <br/> |**visY** (Zeilen MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart und SplineKnot)  <br/> |
||**visInfiniteLineY1** (InfiniteLine-Zeile)  <br/> |
||**visEllipseCenterY** (Ellipsenzeile)  <br/> |
   

