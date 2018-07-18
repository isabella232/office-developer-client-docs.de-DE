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
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796569"
---
# <a name="c-cell-geometry-section"></a>C Cell (Geometry Section)

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Der Winkel der Größenachse des Bogens relativ zu der *X* -Achse des übergeordneten Objekts.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Der erste Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der letzte Knoten eines Splines.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *X* -Koordinate eines Punkts auf der Ellipse; gepaart mit einer *y* -Koordinate, dargestellt durch die Zelle [D](d-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Referenz auf die Zelle C nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . C *j* wobei *i* und *j* = < 1 >, 2, 3...  <br/> |
|| Geometrie *i* . C1 (Zeile Ellipse)  <br/> |
   
Wenn Sie eine Referenz auf die Zelle C aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...  <br/> |
||visRowVertex (Zeile Ellipse)  <br/> |
| Zellenindex:  <br/> |visEccentricityAngle (Zeile EllipticalArcTo)  <br/> |
||visNURBSKnotPrev (Zeile NURBSTo)  <br/> |
||visSplineKnot3 (Zeile SplineStart)  <br/> |
||visEllipseMinorX (Zeile Ellipse)  <br/> |
   

