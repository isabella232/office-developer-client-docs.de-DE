---
title: Zelle "D" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Stellt die Informationen in den verschiedenen Zeilen dar. Diese Tabelle beschreibt die Zelle D anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542499"
---
# <a name="d-cell-geometry-section"></a>Zelle "D" (Abschnitt "Geometry")

Stellt die Informationen in den verschiedenen Zeilen dar. Diese Tabelle beschreibt die Zelle D anhand der Zeile, in der sie sich befindet.
  
|Zeile|Beschreibung|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Das Verhältnis zwischen der größeren und der kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die mit dem Ausdruck "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Wenn der Zellwert auf höchstens 0 bzw. auf größer als 1000 festgelegt wird, können unvorhersehbare Ergebnisse auftreten.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die erste Stärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der Grad eines Splines (eine ganze Zahl von 1 bis 25).  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine  y-Koordinate eines Punkts auf einer Ellipse; gekoppelt mit der x-Koordinate, die durch die [Zelle C dargestellt](c-cell-geometry-section.md) wird.   <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle D anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . D  *j,*            *wobei i*  und  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . D1 (Ellipsenzeile),  *wobei i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle D nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Ellipsenzeile)  <br/> |
| Zellenindex  <br/> |**visAspectRatio** (EllipticalArcTo-Zeile)  <br/> |
||**visNURBSWeightPrev** (NURBSTo-Zeile)  <br/> |
||**visSplineDegree** (SplineStart-Zeile)  <br/> |
||**visEllipseMinorY** (Ellipsenzeile)  <br/> |
   

