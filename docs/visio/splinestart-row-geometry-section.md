---
title: Zeile "SplineStart" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
ms.localizationpriority: medium
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Enthält x- und y-Koordinaten für den zweiten Kontrollpunkt eines Splines, seinen zweiten Knoten, seinen ersten Knoten, den letzten Knoten und den Grad des Splines.
ms.openlocfilehash: 26ef4d10af7dff9376ac214123f1391b38f84dd5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569944"
---
# <a name="splinestart-row-geometry-section"></a>Zeile "SplineStart" (Abschnitt "Geometry")

Enthält  *x-*  und  *y-Koordinaten*  für den zweiten Kontrollpunkt eines Splines, seinen zweiten Knoten, seinen ersten Knoten, den letzten Knoten und den Grad des Splines. 
  
Eine Zeile SplineStart enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die  X-Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die  y-Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Der zweite Knoten des Splines.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Der erste Knoten eines Splines.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Der letzte Knoten eines Splines.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Der Grad eines Splines (eine Ganzzahl von 1 bis 25).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Visio zeigt die Definition eines Splines im Abschnitt Geometry, in dem die Zeile SplineStart enthalten ist, der eine oder mehrere Zeile(n) SplineKnoten nachgestellt ist (sind). Der Zeile SplineStart muss eine andere Art von Zeile vorangehen, etwa MoveTo, die den ersten Kontrollpunkt des Splines anzeigt. Die vorangehende Zeile kann vom Typ LineTo, ArcTo, NURBSTo, PolylineTo oder EllipticalArcTo sein, wenn der Spline einem Segment dieses Typs folgt.
  

