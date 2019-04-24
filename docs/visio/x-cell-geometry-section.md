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
description: Stellt eine x-Koordinate für ein Shape in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 6554000a86a6bf27d343a5647161bbe416725e64
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285112"
---
# <a name="x-cell-geometry-section"></a>Zelle "X" (Abschnitt "Geometrie")

Stellt eine *x* -Koordinate für ein Shape in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet. 
  
|**Zeile**|**Beschreibung**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Wenn die MoveTo-Zeile die erste Zeile im Abschnitt ist, stellt die Zelle X die *x* -Koordinate des ersten Scheitelpunkts eines Pfads dar. Wenn die MoveTo-Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die *x* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Die *x* -Koordinate des Endpunkts eines geraden Linienabschnitts.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die *x* -Koordinate des Endpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *x* -Koordinate des Endpunkts eines elliptischen Bogens.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die *x* -Koordinate des Endpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die *x* -Koordinate des letzten Kontrollpunkts eines nicht einheitlichen rationalen B-Splines (NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Die *x* -Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die *x* -Koordinate eines Kontrollpunkts.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *x* -Koordinate eines Punkts auf der unendlichen Achse.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die *x* -Koordinate des Mittelpunkts der Ellipse.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . X *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . X1 (Endpunkte und Ellipse) wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* = ** 0, 1, 2...  <br/> |
||**visRowVertex** (Zeilen für unendliche und Ellipse)  <br/> |
| Zellenindex:  <br/> |**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polylinie, Zeile SplineStart und SplineKnot Zeilen)  <br/> |
||**visInfiniteLineX1** (Unendliche Zeile)  <br/> |
||**visEllipseCenterX** (Zeile Ellipse)  <br/> |
   

