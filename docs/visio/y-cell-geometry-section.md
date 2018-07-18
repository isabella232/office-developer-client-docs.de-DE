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
description: Stellt einen y-Koordinaten eines Shapes in lokalen Koordinaten dar. Die folgende Tabelle beschreibt die Zelle Y anhand der Zeile in der sie enthalten.
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798464"
---
# <a name="y-cell-geometry-section"></a>Y Cell (Geometry Section)

Stellt eine *y* -Koordinaten eines Shapes in lokalen Koordinaten dar. Die folgende Tabelle beschreibt die Zelle Y anhand der Zeile in der sie enthalten. 
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Wenn die Zeile MoveTo die erste Zeile im Abschnitt ist, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts eines Pfads. Wenn die Zeile MoveTo zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Endscheitelpunkts eines elliptischen Bogens.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Endscheitelpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die *y* -Koordinate des letzten Kontrollpunkts von einer nicht einheitlichen rationalen B-Spline (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Die *y* -Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die *y* -Koordinate eines Kontrollpunkts.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *y -* Koordinate eines Punkts auf der unendlichen Linie.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die *y* -Koordinate des Mittelpunkts der Ellipse.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Y aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . Y *j* wobei *i* und *j* = < 1 >, 2, 3...  <br/> |
|| Geometrie *i* . Y1 (Zeilen UnendlicheLinie und Ellipse) wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Y aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...  <br/> |
||visRowVertex (Zeilen InfiniteLine und Ellipse)  <br/> |
| Zellenindex:  <br/> |visY (Zeilen MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart und SplineKnot)  <br/> |
||visInfiniteLineY1 (Zeile InfiniteLine)  <br/> |
||visEllipseCenterY (Zeile Ellipse)  <br/> |
   

