---
title: Zeile "EllipticalArcTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Enthält die x-und y-Koordinaten des Endpunkts eines elliptischen Bogens, die x-und y-Koordinaten der Steuerpunkte des Bogens, den Winkel von der x-Achse zur Hauptachse der Ellipse und das Verhältnis zwischen Haupt-und Nebenachsen der Ellipse.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345675"
---
# <a name="ellipticalarcto-row-geometry-section"></a>Zeile "EllipticalArcTo" (Abschnitt "Geometry")

Enthält die *x* -und *y* -Koordinaten des Endpunkts eines elliptischen Bogens, die *x* -und *y* -Koordinaten der Kontrollpunkte des Bogens, den Winkel von der *x* -Achse zur Hauptachse der Ellipse und das Verhältnis zwischen dem großen und dem Mino r-Achsen. 
  
Eine Zeile EllipticalArcTo enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *x* -Koordinate des Endpunkts eines Bogens.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Endpunkts eines Bogens.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die *x* -Koordinate des Kontrollpunkts des Bogens; ein Punkt auf dem Bogen. Der Steuerpunkt befindet sich am besten in der Mitte zwischen dem Anfangs-und Endscheitel des Bogens. Andernfalls kann der Bogen zu einer extremen Größe anwachsen, um den Kontrollpunkt mit unvorhersehbaren Ergebnissen zu durchlaufen.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Kontrollpunkts eines Bogens.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Der Winkel der Hauptachse eines Bogens relativ zur *x* -Achse des übergeordneten Elements.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.  <br/> |
   

