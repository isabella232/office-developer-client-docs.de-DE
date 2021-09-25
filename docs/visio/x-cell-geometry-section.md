---
title: Zelle "X" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
ms.localizationpriority: medium
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Stellt eine X-Koordinate eines Shapes in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 1435e07bc2c2d02f971f0fa083638acb903d0114
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553592"
---
# <a name="x-cell-geometry-section"></a>Zelle "X" (Abschnitt "Geometrie")

Stellt  eine X-Koordinate eines Shapes in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet. 
  
|Zeile|Beschreibung|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> | Wenn die Zeile MoveTo  die erste Zeile im Abschnitt ist, stellt die Zelle X die X-Koordinate des ersten Scheitelpunkts eines Pfads dar. Wenn die Zeile MoveTo zwischen zwei Zeilen angezeigt wird, stellt die Zelle  *X*  die X-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.  <br/> |
|[Lineto](lineto-row-geometry-section.md) <br/> | Die  X-Koordinate des Endscheitelpunkts eines geraden Liniensegments.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die  X-Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die  X-Koordinate des Endscheitelpunkts eines elliptischen Bogens.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die  X-Koordinate des Endscheitelpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die  X-Koordinate des letzten Kontrollpunkts eines nicht fähigen rationalen B-Splines (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Die  X-Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die  X-Koordinate eines Kontrollpunkts.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine  X-Koordinate eines Punkts auf der unendlichen Linie.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die  X-Koordinate des Mittelpunkts der Ellipse.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle X anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . X  *j*            where  *i*  and  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . X1 (InfiniteLine- und Ellipse-Zeilen), wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle X anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j* where *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine- und Ellipse-Zeilen)  <br/> |
| Zellenindex:  <br/> |**visX** (Zeilen "MoveTo", "LineTo", "ArcTo", "EllipticalArcTo", "NURBSTo", "Polyline", "SplineStart" und "SplineKnot")  <br/> |
||**visInfiniteLineX1** (Zeile "InfiniteLine")  <br/> |
||**visEllipseCenterX** (Zeile "Ellipse")  <br/> |
   

