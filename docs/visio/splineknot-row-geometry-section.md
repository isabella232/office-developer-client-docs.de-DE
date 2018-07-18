---
title: Zeile "SplineKnot" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3050
localization_priority: Normal
ms.assetid: 9fbae27d-4f1b-c5f7-aacb-16f359331e83
description: Enthält X- und y-Koordinaten für den Kontrollpunkt eines Splines und den Knoten eines Splines.
ms.openlocfilehash: 297889208e064870dd37ed45a17fef7cb4b333b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798180"
---
# <a name="splineknot-row-geometry-section"></a>SplineKnot Row (Geometry Section)

Enthält die *X* - und *y* -Koordinaten für den Kontrollpunkt eines Splines und den Knoten eines Splines. 
  
Eine Zeile SplineKnot enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *X* -Koordinate eines Kontrollpunkts.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate eines Kontrollpunkts.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).  <br/> |
   
## <a name="remarks"></a>Hinweise

Visio zeigt die Definition eines Splines im Abschnitt Geometry, in dem die Zeile SplineStart enthalten ist, der eine oder mehrere Zeile(n) SplineKnoten nachgestellt ist (sind). Der Zeile SplineStart muss eine andere Art von Zeile vorangehen, etwa MoveTo, die den ersten Kontrollpunkt des Splines anzeigt. Die vorangehende Zeile kann vom Typ LineTo, ArcTo, NURBSTo, PolylineTo oder EllipticalArcTo sein, wenn der Spline einem Segment dieses Typs folgt.
  

