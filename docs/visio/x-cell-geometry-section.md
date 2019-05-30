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
description: Stellt eine x-Koordinate eines Shapes in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 2b3303533db446780ef797844ac5e1438cec242f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538214"
---
# <a name="x-cell-geometry-section"></a>Zelle "X" (Abschnitt "Geometrie")

Stellt eine *x* -Koordinate eines Shapes in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet. 
  
|Row|Beschreibung|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Wenn die MoveTo-Zeile die erste Zeile im Abschnitt ist, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts eines Pfads dar. Wenn die Zeile MoveTo zwischen zwei Zeilen angezeigt wird, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Die *x* -Koordinate des letzten Scheitelpunkts eines geraden Linie Segments.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die *x* -Koordinate des letzten Scheitelpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *x* -Koordinate des letzten Scheitelpunkts eines elliptischen Bogens.  <br/> |
|[PolyLineTo](polylineto-row-geometry-section.md) <br/> | Die *x* -Koordinate des letzten Scheitelpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die *x* -Koordinate des letzten Kontrollpunktes eines nicht einheitlichen rationalen B-Splines (NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Die *x* -Koordinate des zweiten Kontrollpunktes eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die *x* -Koordinate eines Kontrollpunktes.  <br/> |
|[Zeile InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *x* -Koordinate eines Points auf der unendlichen Reihe.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die *x* -Koordinate des Mittelpunkts der Ellipse.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . X *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . X1 (endlos-und Ellipsen Zeilen) wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* , wobei *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Endlos-und Ellipsen Zeilen)  <br/> |
| Zellenindex:  <br/> |**visX** (MoveTo-, LineTo-, ArcTo-, EllipticalArcTo-, NURBSTo-, Polyline-, Zeile SplineStart-und SplineKnot-Zeilen)  <br/> |
||**visInfiniteLineX1** (Endlos Zeile)  <br/> |
||**visEllipseCenterX** (Ellipsen Zeile)  <br/> |
   

