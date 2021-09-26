---
title: Zeile "EllipticalArcTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
ms.localizationpriority: medium
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Enthält x- und y-Koordinaten des Endpunkts eines elliptischen Bogens, x- und y-Koordinaten der Kontrollpunkte im Bogen, Winkel von der x-Achse zur Hauptachse der Ellipse und Verhältnis zwischen der Haupt- und Nebenachse der Ellipse.
ms.openlocfilehash: 53bc69b8047a21b0e0cb4c6c2d567de3d8dd69e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612855"
---
# <a name="ellipticalarcto-row-geometry-section"></a>Zeile "EllipticalArcTo" (Abschnitt "Geometry")

Enthält  *x-*  und  *y-Koordinaten*  des Endpunkts eines elliptischen Bogens,  *x-*  und  *y-Koordinaten*  der Kontrollpunkte im Bogen, Winkel von der  *x-Achse*  zur Hauptachse der Ellipse und Verhältnis zwischen der Haupt- und Nebenachse der Ellipse. 
  
Eine Zeile EllipticalArcTo enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die  X-Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die  y-Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die  X-Koordinate des Kontrollpunkts des Bogens; ein Punkt auf dem Bogen. Der Kontrollpunkt befindet sich am besten etwa in der Mitte zwischen den Anfangs- und Endscheitelpunkten des Bogens. Andernfalls kann der Bogen zu einer extrem großen Größe werden, um den Kontrollpunkt zu durchlaufen, was zu unvorhersehbaren Ergebnissen führt.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Die  y-Koordinate des Kontrollpunkts eines Bogens.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Der Winkel der Hauptachse eines Bogens relativ zur  *X-Achse*  des übergeordneten Bereichs.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.  <br/> |
   

