---
title: Zelle "C" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
ms.localizationpriority: medium
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: 0eb4e933e8d27bdc440ce7e386388b37f2108f5d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608606"
---
# <a name="c-cell-geometry-section"></a>Zelle "C" (Abschnitt "Geometrie")

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|Zeile|Beschreibung|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Der Winkel der Hauptachse eines Bogens relativ zur  *X-Achse*  des übergeordneten Bereichs.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Der erste Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der letzte Knoten eines Splines.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine  X-Koordinate eines Punkts auf einer Ellipse; gepaart mit der y-Koordinate, dargestellt durch die Zelle [D.](d-cell-geometry-section.md)   <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle C anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . C  *j*            where  *i*  and  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . C1 (Ellipse-Zeile)  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle C anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j* where *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (Ellipse-Zeile)  <br/> |
| Zellenindex:  <br/> |**visEccentricityAngle** (Zeile "EllipticalArcTo")  <br/> |
||**visNURBSKnotPrev** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot3** (SplineStart-Zeile)  <br/> |
||**visEllipseMinorX** (Zeile "Ellipse")  <br/> |
   

