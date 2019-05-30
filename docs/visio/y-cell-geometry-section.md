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
description: Stellt eine y-Koordinate eines Shapes in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 7dea96b544c84f09abe1d72304da0bacaa09432f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540490"
---
# <a name="y-cell-geometry-section"></a>Zelle "Y" (Abschnitt "Geometrie")

Stellt eine *y* -Koordinate eines Shapes in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet. 
  
|Row|Beschreibung|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Wenn die MoveTo-Zeile die erste Zeile im Abschnitt ist, stellt die Zelle y die *y* -Koordinate des ersten Scheitelpunkts eines Pfads dar. Wenn die MoveTo-Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle y die *y* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Die *y* -Koordinate des letzten Scheitelpunkts eines geraden Linie Segments.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die *y* -Koordinate des letzten Scheitelpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *y* -Koordinate des letzten Scheitelpunkts eines elliptischen Bogens.  <br/> |
|[PolyLineTo](polylineto-row-geometry-section.md) <br/> | Die *y* -Koordinate des letzten Scheitelpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die *y* -Koordinate des letzten Kontrollpunktes eines nicht einheitlichen rationalen B-Splines (NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Die *y* -Koordinate des zweiten Kontrollpunktes eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die *y* -Koordinate eines Kontrollpunktes.  <br/> |
|[Zeile InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *y-* Koordinate eines Points auf der unendlichen Leine.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die *y* -Koordinate des Mittelpunkts der Ellipse.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Y aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . Y *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . Y1 (Zeilen endlos und Ellipse) wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Y aus einem Programm aus nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* , wobei *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Endlos-und Ellipsen Zeilen)  <br/> |
| Zellenindex:  <br/> |**visY** (MoveTo-, LineTo-, ArcTo-, EllipticalArcTo-, NURBSTo-, Polyline-, Zeile SplineStart-und SplineKnot-Zeilen)  <br/> |
||**visInfiniteLineY1** (Endlos Zeile)  <br/> |
||**visEllipseCenterY** (Ellipsen Zeile)  <br/> |
   

