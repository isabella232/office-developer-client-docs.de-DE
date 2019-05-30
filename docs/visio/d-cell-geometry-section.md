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
  
|Row|Beschreibung|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Das Verhältnis zwischen der größeren und der kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die mit dem Ausdruck "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Wenn der Zellwert auf höchstens 0 bzw. auf größer als 1000 festgelegt wird, können unvorhersehbare Ergebnisse auftreten.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die erste Stärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Der Grad eines Splines (eine ganze Zahl von 1 bis 25).  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *y* -Koordinate eines Kommas auf einer Ellipse; gepaart mit der *x* -Koordinate, dargestellt durch die Zelle [C](c-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle D aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . D *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . D1 (Ellipsen Zeile) wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle D aus einem Programm aus nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* , wobei *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Ellipsen Zeile)  <br/> |
| Zellenindex  <br/> |**visAspectRatio** (EllipticalArcTo-Zeile)  <br/> |
||**visNURBSWeightPrev** (NURBSTo-Zeile)  <br/> |
||**visSplineDegree** (Zeile SplineStart-Zeile)  <br/> |
||**visEllipseMinorY** (Ellipsen Zeile)  <br/> |
   

