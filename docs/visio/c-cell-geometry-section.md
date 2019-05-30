---
title: Zelle "C" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541890"
---
# <a name="c-cell-geometry-section"></a>Zelle "C" (Abschnitt "Geometrie")

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|Row|Beschreibung|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Der Winkel der Hauptachse eines Bogens relativ zur *x* -Achse des übergeordneten Elements.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Der erste Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Der letzte Knoten eines Splines.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *x* -Koordinate eines Points auf einer Ellipse; gepaart mit der *y* -Koordinate, dargestellt durch die Zelle [D](d-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle C aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . C *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . C1 (Ellipsen Zeile)  <br/> |
   
Wenn Sie einen Verweis auf die Zelle C aus einem Programm aus nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* , wobei *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Ellipsen Zeile)  <br/> |
| Zellenindex:  <br/> |**visEccentricityAngle** (EllipticalArcTo-Zeile)  <br/> |
||**visNURBSKnotPrev** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot3** (Zeile SplineStart-Zeile)  <br/> |
||**visEllipseMinorX** (Ellipsen Zeile)  <br/> |
   

