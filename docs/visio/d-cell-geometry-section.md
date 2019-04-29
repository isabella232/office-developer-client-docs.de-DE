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
ms.openlocfilehash: 1da6ac19e6a50ea87f07bf3e3c9f96378b512ba8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424378"
---
# <a name="d-cell-geometry-section"></a>Zelle "D" (Abschnitt "Geometry")

Stellt die Informationen in den verschiedenen Zeilen dar. Diese Tabelle beschreibt die Zelle D anhand der Zeile, in der sie sich befindet.
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Das Verhältnis zwischen der größeren und der kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die mit dem Ausdruck "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Wenn der Zellwert auf höchstens 0 bzw. auf größer als 1000 festgelegt wird, können unvorhersehbare Ergebnisse auftreten.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die erste Stärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Der Grad eines Splines (eine ganze Zahl von 1 bis 25).  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *y* -Koordinate eines Punkts auf einer Ellipse; gepaart mit der *x* -Koordinate, dargestellt durch die Zelle [C](c-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle D aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . D *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . D1 (Ellipsen Zeile) wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle D nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* = ** 0, 1, 2...  <br/> |
||**visRowVertex** (Zeile Ellipse)  <br/> |
| Zellenindex  <br/> |**visAspectRatio** (EllipticalArcTo-Zeile)  <br/> |
||**visNURBSWeightPrev** (NURBSTo-Zeile)  <br/> |
||**visSplineDegree** (Zeile SplineStart-Zeile)  <br/> |
||**visEllipseMinorY** (Zeile Ellipse)  <br/> |
   

