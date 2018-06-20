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
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796763"
---
# <a name="d-cell-geometry-section"></a>D Cell (Geometry Section)

Stellt die Informationen in den verschiedenen Zeilen dar. Diese Tabelle beschreibt die Zelle D anhand der Zeile, in der sie sich befindet.
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die erste Stärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der Grad eines Splines (eine Ganzzahl von 1 bis 25).  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *y* -Koordinate eines Punkts auf der Ellipse; gepaart mit einer *X* -Koordinate, dargestellt durch die Zelle [C](c-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle D nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . D *j* wobei *i* und *j* = < 1 >, 2, 3...  <br/> |
|| Geometrie *i* . D1 (Zeile Ellipse) wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle D aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Ellipsenzeile)  <br/> |
| Zellenindex  <br/> |**visAspectRatio** (Zeile EllipticalArcTo)  <br/> |
||**visNURBSWeightPrev** (Zeile NURBSTo)  <br/> |
||**visSplineDegree** (Zeile SplineStart)  <br/> |
||**visEllipseMinorY** (Ellipsenzeile)  <br/> |
   

