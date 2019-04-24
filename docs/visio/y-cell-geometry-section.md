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
description: Stellt eine y-Koordinate für ein Shape in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 9e823b8d21682b419a70ce498016abf575f36f6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342812"
---
# <a name="y-cell-geometry-section"></a>Zelle "Y" (Abschnitt "Geometrie")

Stellt eine *y* -Koordinate für ein Shape in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet. 
  
|**Zeile**|**Beschreibung**|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Wenn die MoveTo-Zeile die erste Zeile im Abschnitt ist, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts eines Pfads dar. Wenn die MoveTo-Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Endpunkts eines geraden Linienabschnitts.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Endpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Endpunkts eines elliptischen Bogens.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Endpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die *y* -Koordinate des letzten Kontrollpunkts eines nicht einheitlichen rationalen B-Splines (NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Die *y* -Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die *y* -Koordinate eines Kontrollpunkts.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *y-* Koordinate eines Punkts auf der unendlichen Achse.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die *y* -Koordinate des Mittelpunkts der Ellipse.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Y aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . Y *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . Y1 (Zeilen für unendliche und Ellipse) wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Y nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* = ** 0, 1, 2...  <br/> |
||**visRowVertex** (Zeilen für unendliche und Ellipse)  <br/> |
| Zellenindex:  <br/> |**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polylinie, Zeile SplineStart und SplineKnot Zeilen)  <br/> |
||**visInfiniteLineY1** (Unendliche Zeile)  <br/> |
||**visEllipseCenterY** (Zeile Ellipse)  <br/> |
   

