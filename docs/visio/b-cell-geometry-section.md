---
title: Zelle "B" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: ff032b5af2918ec9865360ede5c3d76e8e872e9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423307"
---
# <a name="b-cell-geometry-section"></a>Zelle "B" (Abschnitt "Geometry")

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die *y* -Koordinate des Kontrollpunkts eines Bogens.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die zuletzt verwendete Linienstärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Der erste Knoten eines Splines.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine *y* -Koordinate eines Punkts auf einer unendlichen Achse. gepaart mit einer *x* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *y* -Koordinate eines Punkts auf einer Ellipse; gepaart mit einer *x* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle B aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . B *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . B1 (Zeilen für unendliche und Ellipse)  <br/> |
   
Wenn Sie einen Verweis auf die Zelle B aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* = ** 0, 1, 2...  <br/> |
||**visRowVertex** (Zeilen für unendliche und Ellipse)  <br/> |
| Zellenindex:  <br/> |**visControlX** (EllipticalArcTo-Zeile)  <br/> |
||**visControlY** (EllipticalArcTo-Zeile)  <br/> |
||**visNURBSWeight** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot2** (Zeile SplineStart-Zeile)  <br/> |
||**visInfiniteLineY2** (Unendliche Zeile)  <br/> |
||**visEllipseMajorY** (Zeile Ellipse)  <br/> |
   

