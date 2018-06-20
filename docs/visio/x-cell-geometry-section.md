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
description: Stellt eine X-Koordinate eines Shapes in lokalen Koordinaten. Die folgende Tabelle beschreibt die Zelle X anhand der Zeile in der sie enthalten.
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798429"
---
# <a name="x-cell-geometry-section"></a>X Cell (Geometry Section)

Stellt eine *X* -Koordinate eines Shapes in lokalen Koordinaten. Die folgende Tabelle beschreibt die Zelle X anhand der Zeile in der sie enthalten. 
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Wenn die Zeile MoveTo die erste Zeile im Abschnitt ist, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts eines Pfads. Wenn die Zeile MoveTo zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Die *X* -Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die *X* -Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *X* -Koordinate des Endscheitelpunkts eines elliptischen Bogens.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die *X* -Koordinate des Endscheitelpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die *X* -Koordinate des letzten Kontrollpunkts von einer nicht einheitlichen rationalen B-Spline (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Die *X* -Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die *X* -Koordinate eines Kontrollpunkts.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *X* -Koordinate eines Punkts auf der unendlichen Linie.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die *X* -Koordinate des Mittelpunkts der Ellipse.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle X nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . X *j* wobei *i* und *j* = < 1 >, 2, 3...  <br/> |
|| Geometrie *i* . X1 (Zeilen UnendlicheLinie und Ellipse) wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Zeilen UnendlicheLinie und Ellipse)  <br/> |
| Zellenindex:  <br/> |**visX** (Zeilen MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart und SplineKnot)  <br/> |
||**visInfiniteLineX1** (Zeile InfiniteLine)  <br/> |
||**visEllipseCenterX** (Ellipsenzeile)  <br/> |
   

