---
title: Zeile "SplineStart" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Enthält X- und y-Koordinaten des zweiten Kontrollpunkts eines Splines, dessen zweiten Knoten, dessen ersten Knoten, der letzte Knoten und den Grad eines Splines.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798182"
---
# <a name="splinestart-row-geometry-section"></a>SplineStart Row (Geometry Section)

Enthält die *X* - und *y* -Koordinaten des zweiten Kontrollpunkts eines Splines, dessen zweiten Knoten, dessen ersten Knoten, der letzte Knoten und den Grad eines Splines. 
  
Eine Zeile SplineStart enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *X* -Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Der zweite Knoten des Splines.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Der erste Knoten eines Splines.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Der letzte Knoten eines Splines.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Der Grad eines Splines (eine Ganzzahl von 1 bis 25).  <br/> |
   
## <a name="remarks"></a>Hinweise

Visio zeigt die Definition eines Splines im Abschnitt Geometry, in dem die Zeile SplineStart enthalten ist, der eine oder mehrere Zeile(n) SplineKnoten nachgestellt ist (sind). Der Zeile SplineStart muss eine andere Art von Zeile vorangehen, etwa MoveTo, die den ersten Kontrollpunkt des Splines anzeigt. Die vorangehende Zeile kann vom Typ LineTo, ArcTo, NURBSTo, PolylineTo oder EllipticalArcTo sein, wenn der Spline einem Segment dieses Typs folgt.
  

