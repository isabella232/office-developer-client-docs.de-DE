---
title: Abschnitt "Geometrie"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Enthält Zeilen, in denen die Koordinaten der Scheitelpunkte für die Linien und Bögen, die das Shape bilden aufgeführt.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797085"
---
# <a name="geometry-section"></a>Geometry Section

Enthält Zeilen, in denen die Koordinaten der Scheitelpunkte für die Linien und Bögen, die das Shape bilden aufgeführt. 
  
Die Geometrie eines Shapes kann in mehreren **geometrischen** Abschnitte ausgedrückt werden. Mehrere Pfade können hilfreich sein, wenn mehrere Pfade über verschiedene Eigenschaften (z. B. [Bild Clipping](clippingpath-cell-foreign-image-info-section.md) Pfade) verfügen. 
  
## <a name="remarks"></a>Bemerkungen

Der Abschnitt **"Geometry"** enthält die folgenden Zeilentypen. Weitere Informationen hierzu finden Sie unter den Themen Zeile. 
  
|**Row**|**Beschreibung**|
|:-----|:-----|
|[MoveTo](moveto-row-geometry-section.md) <br/> |Verschieben zu einer Koordinate.  <br/> |
|[LineTo](lineto-row-geometry-section.md) <br/> |Eine Linie bis zu einer Koordinate zeichnen.  <br/> |
|[ArcTo](arcto-row-geometry-section.md) <br/> |Einen kreisförmigen Bogen bis zu einer Koordinate zeichnen.  <br/> |
|[EllipticalArcTo](ellipticalarcto-row-geometry-section.md) <br/> |Einen elliptischen Bogen bis zu einer Koordinate zeichnen.  <br/> |
|[PolylineTo](polylineto-row-geometry-section.md) <br/> |Eine Polylinie oder aufeinander folgende Linien bis zu einer Koordinate zeichnen.  <br/> |
|[NURBSTo](nurbsto-row-geometry-section.md) <br/> |Zeichnen Sie ein nicht einheitlichen rationales B-Spline (NURBS) bis zu einer Koordinate.  <br/> |
|[SplineStart](splinestart-row-geometry-section.md) <br/> |Ein Spline beginnen.  <br/> |
|[SplineKnot](splineknot-row-geometry-section.md) <br/> |Ein Splinesegment bis zu einer Knotenkoordinate zeichnen.  <br/> |
|[InfiniteLine](infiniteline-row-geometry-section.md) <br/> |Eine unendliche Linie von einer Koordinate zu einer anderen zeichnen.  <br/> |
|[Ellipse](ellipse-row-geometry-section.md) <br/> |Eine Ellipse von einer Mittelkoordinate und einer großen/kleinen Achse zeichnen.  <br/> |
|[RelCubBezTo](relcubbezto-row-geometry-section.md) <br/> |Zeichnen Sie eine kubische Bézierkurve relativ zu der Breite und Höhe des Shapes.  <br/> |
|[RelEllipticalArcTo](relellipticalarcto-row-geometry-section.md) <br/> |Zeichnen Sie einen elliptischen Bogen bis zu einer Koordinate relativ zur Höhe und Breite der Form.  <br/> |
|[RelLineTo](rellineto-row-geometry-section.md) <br/> |Zeichnen Sie eine Linie einer relativen Koordinaten, die Höhe und Breite eines Shapes.  <br/> |
|[RelMoveTo](relmoveto-row-geometry-section.md) <br/> |Verschieben Sie zu einer Koordinate relativ zu der Breite und Höhe des Shapes.  <br/> |
|[RelQuadBezTo](relquadbezto-row-geometry-section.md) <br/> |Zeichnet eine quadratische Bézierkurve relativ zu der Breite und Höhe des Shapes.  <br/> |
   
Wenn Sie einen Zeilentyp in diesem Abschnitt ändern möchten, klicken Sie mit der rechten Maustaste auf die Zeile, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**. 
  

