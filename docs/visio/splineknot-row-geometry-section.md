---
title: Zeile "SplineKnot" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
ms.localizationpriority: medium
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Enthält x- und y-Koordinaten für den Kontrollpunkt eines Splines und den Knoten eines Splines.
ms.openlocfilehash: e2fb84bbd269768e3bd7f85874bb8f8865ea8d94
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559460"
---
# <a name="splineknot-row-geometry-section"></a>Zeile "SplineKnot" (Abschnitt "Geometry")

Enthält  *x-*  und  *y-Koordinaten*  für den Kontrollpunkt eines Splines und den Knoten eines Splines. 
  
Eine Zeile SplineKnot enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die  X-Koordinate eines Kontrollpunkts.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die  y-Koordinate eines Kontrollpunkts.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Visio zeigt die Definition eines Splines im Abschnitt Geometry, in dem die Zeile SplineStart enthalten ist, der eine oder mehrere Zeile(n) SplineKnoten nachgestellt ist (sind). Der Zeile SplineStart muss eine andere Art von Zeile vorangehen, etwa MoveTo, die den ersten Kontrollpunkt des Splines anzeigt. Die vorangehende Zeile kann vom Typ LineTo, ArcTo, NURBSTo, PolylineTo oder EllipticalArcTo sein, wenn der Spline einem Segment dieses Typs folgt.
  

