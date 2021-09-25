---
title: Zelle "Y" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
ms.localizationpriority: medium
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Stellt eine y-Koordinate auf einem Shape in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: db663e959e0204630cdd2316f906792227a44a67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59581735"
---
# <a name="y-cell-geometry-section"></a>Zelle "Y" (Abschnitt "Geometrie")

Stellt  eine y-Koordinate auf einem Shape in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet. 
  
|Zeile|Beschreibung|
|:-----|:-----|
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Wenn die Zeile MoveTo die erste Zeile im Abschnitt ist, stellt die Zelle  *Y*  die Y-Koordinate des ersten Scheitelpunkts eines Pfads dar. Wenn die Zeile MoveTo zwischen zwei Zeilen angezeigt wird, stellt die Zelle  *Y*  die Y-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.  <br/> |
|[Lineto](lineto-row-geometry-section.md) <br/> | Die  y-Koordinate des Endscheitelpunkts eines geraden Liniensegments.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> | Die  y-Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die  y-Koordinate des Endscheitelpunkts eines elliptischen Bogens.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> | Die  y-Koordinate des Endscheitelpunkts einer Polylinie.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die  y-Koordinate des letzten Kontrollpunkts eines nicht fähigen rationalen B-Splines (NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Die  y-Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> | Die  y-Koordinate eines Kontrollpunkts.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine  *Y-Koordinate*  eines Punkts auf der unendlichen Linie.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Die  y-Koordinate des Mittelpunkts der Ellipse.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle Y anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . Y1 (InfiniteLine- und Ellipse-Zeilen), wobei  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j* where *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine- und Ellipse-Zeilen)  <br/> |
| Zellenindex:  <br/> |**visY** (Zeilen "MoveTo", "LineTo", "ArcTo", "EllipticalArcTo", "NURBSTo", "Polyline", "SplineStart" und "SplineKnot")  <br/> |
||**visInfiniteLineY1** (Zeile "InfiniteLine")  <br/> |
||**visEllipseCenterY** (Zeile "Ellipse")  <br/> |
   

