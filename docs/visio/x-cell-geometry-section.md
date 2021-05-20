---
title: Zelle "X" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Stellt eine x-Koordinate auf einer Form in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 2b3303533db446780ef797844ac5e1438cec242f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538214"
---
# <a name="x-cell-geometry-section"></a>Zelle "X" (Abschnitt "Geometrie")

Stellt  eine x-Koordinate auf einer Form in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet. 
  
|Zeile|Beschreibung|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Wenn die MoveTo-Zeile die erste Zeile im Abschnitt  ist, stellt die Zelle X die x-Koordinate des ersten Scheitelpunkts eines Pfads dar. Wenn die MoveTo-Zeile zwischen zwei Zeilen  angezeigt wird, stellt die Zelle X die x-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Die  x-Koordinate des endenden Scheitelpunkts eines geraden Abschnitts.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die  x-Koordinate des endenden Scheitelpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die  x-Koordinate des endenden Scheitelpunkts eines elliptischen Bogens.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die  x-Koordinate des endenden Scheitelpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die  x-Koordinate des letzten Kontrollpunkts eines nicht einheitsgeformten rationalen B-Splines (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Die  x-Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die  x-Koordinate eines Kontrollpunkts.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine  x-Koordinate eines Punkts auf der unendlichen Linie.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die  x-Koordinate der Mitte der Ellipse.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . X  *j,*            *wobei i*  und  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . X1 (InfiniteLine- und Ellipsenzeilen), wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die X-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine- und Ellipsenzeilen)  <br/> |
| Zellenindex:  <br/> |**visX** (Zeilen MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart und SplineKnot)  <br/> |
||**visInfiniteLineX1** (InfiniteLine-Zeile)  <br/> |
||**visEllipseCenterX** (Ellipsenzeile)  <br/> |
   

