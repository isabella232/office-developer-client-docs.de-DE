---
title: Abschnitt "Geometrie"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
ms.localizationpriority: medium
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Enthält Zeilen, die die Koordinaten der Scheitelpunkte für die Linien und Bögen auflisten, aus denen das Shape besteht.
ms.openlocfilehash: 38418376f6296fb3b6f1bbb4e9722421dfcf2440
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598577"
---
# <a name="geometry-section"></a>Abschnitt "Geometrie"

Enthält Zeilen, die die Koordinaten der Scheitelpunkte für die Linien und Bögen auflisten, aus denen das Shape besteht. 
  
Die Geometrie eines Shapes kann in mehreren **Geometry-Abschnitten** ausgedrückt werden. Mehrere Pfade können nützlich sein, wenn mehrere Pfade unterschiedliche Eigenschaften haben (z. B. [Bildclipingpfade).](clippingpath-cell-foreign-image-info-section.md) 
  
## <a name="remarks"></a>HinwBemerkungeneise

Der Abschnitt **Geometry** enthält die folgenden Zeilentypen. Weitere Details finden Sie unter den Zellenthemen. 
  
|Zeile|Beschreibung|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Verschieben zu einer Koordinate.  <br/> |
|[Lineto](lineto-row-geometry-section.md) <br/> |Eine Linie bis zu einer Koordinate zeichnen.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Einen kreisförmigen Bogen bis zu einer Koordinate zeichnen.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Einen elliptischen Bogen bis zu einer Koordinate zeichnen.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Eine Polylinie oder aufeinander folgende Linien bis zu einer Koordinate zeichnen.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Zeichnen sie einen nicht einheitlichen rationalen B-Spline (NURBS) in eine Koordinate.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Ein Spline beginnen.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Ein Splinesegment bis zu einer Knotenkoordinate zeichnen.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Eine unendliche Linie von einer Koordinate zu einer anderen zeichnen.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> |Eine Ellipse von einer Mittelkoordinate und einer großen/kleinen Achse zeichnen.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Zeichnen Sie eine kubische Bézierkurve relativ zur Breite und Höhe der Form.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Zeichnen Sie einen elliptischen Bogen auf eine Koordinate relativ zur Höhe und Breite des Shapes.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Zeichnen einer Linie zu einer Koordinate relativ zur Höhe und Breite eines Shapes.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Wechseln zu einer Koordinate relativ zur Breite und Höhe des Shapes.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Zeichnet eine quadratische Bézierkurve relativ zur Breite und Höhe der Form.  <br/> |
   
Wenn Sie einen Zeilentyp in diesem Abschnitt ändern möchten, klicken Sie mit der rechten Maustaste auf die Zeile, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**. 
  

