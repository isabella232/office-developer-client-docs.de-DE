---
title: Zelle "B" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
ms.localizationpriority: medium
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: ae275534871245c78df09a3b94fb51cadf7c10cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603851"
---
# <a name="b-cell-geometry-section"></a>Zelle "B" (Abschnitt "Geometry")

Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
  
|Zeile|Beschreibung|
|:-----|:-----|
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> | Die  y-Koordinate des Kontrollpunkts eines Bogens.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> | Die zuletzt verwendete Linienstärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> | Der erste Knoten eines Splines.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> | Eine  y-Koordinate eines Punkts auf einer unendlichen Linie; gepaart mit einer X-Koordinate, dargestellt durch die Zelle [A.](a-cell-geometry-section.md)   <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> | Eine  y-Koordinate eines Punkts auf einer Ellipse; gepaart mit einer X-Koordinate, dargestellt durch die Zelle [A.](a-cell-geometry-section.md)   <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie zum Abrufen eines Verweises auf die Zelle B anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometry  *i*  . B  *j*            where  *i*  and  *j*  = <1>, 2, 3...  <br/> |
|| Geometry  *i*  . B1 (InfiniteLine- und Ellipse-Zeilen)  <br/> |
   
Um einen Verweis auf die Zelle B anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex**  +   *j* where *j* = 0, 1, 2...  <br/> |
||**visRowVertex** (InfiniteLine- und Ellipse-Zeilen)  <br/> |
| Zellenindex:  <br/> |**visControlX** (Zeile "EllipticalArcTo")  <br/> |
||**visControlY** (Zeile "EllipticalArcTo")  <br/> |
||**visNURBSWeight** (NURBSTo-Zeile)  <br/> |
||**visSplineKnot2** (SplineStart-Zeile)  <br/> |
||**visInfiniteLineY2** (Zeile "InfiniteLine")  <br/> |
||**visEllipseMajorY** (Zeile "Ellipse")  <br/> |
   

