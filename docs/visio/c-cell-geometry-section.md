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
ms.openlocfilehash: 5599c09ad3656653c486d7feff9aed2ee89e4614
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413367"
---
# <a name="c-cell-geometry-section"></a>Zelle "C" (Abschnitt "Geometrie")

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Der Winkel der Hauptachse eines Bogens relativ zur *x* -Achse des übergeordneten Elements.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Der erste Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[Zeile SplineStart](splinestart-row-geometry-section.md) <br/> | Der letzte Knoten eines Splines.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine *x* -Koordinate eines Punkts auf einer Ellipse; gepaart mit der *y* -Koordinate, dargestellt durch die Zelle [D](d-cell-geometry-section.md) .  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle C aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . C *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
|| Geometrie *i* . C1 (Zeile Ellipse)  <br/> |
   
Wenn Sie einen Verweis auf die Zelle C aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* = ** 0, 1, 2...  <br/> |
||**visRowVertex** (Zeile Ellipse)  <br/> |
| Zellenindex:  <br/> |**visEccentricityAngle** (EllipticalArcTo-Zeile)  <br/> |
||**visNURBSKnotPrev** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot3** (Zeile SplineStart-Zeile)  <br/> |
||**visEllipseMinorX** (Zeile Ellipse)  <br/> |
   

