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
description: Enthält X- und y-Koordinaten des eines elliptischen Bogens Endpunkt, X- und y-Koordinaten der Kontrollpunkte des Bogens, den Winkel von X-Achse zu großen Achse der Ellipse und das Verhältnis zwischen der Ellipse Haupt- und Hilfsintervalle Achsen.
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796925"
---
# <a name="ellipticalarcto-row-geometry-section"></a>EllipticalArcTo Row (Geometry Section)

Enthält die *X* - und *y* - Koordinaten des Endpunkts eines elliptischen Bogens, *X* - und *y* -Koordinaten der Kontrollpunkte des Bogens, Winkel von der *x* -Achse zu großen Achse der Ellipse und das Verhältnis zwischen der Ellipse Haupt- und Mino R Achsen. 
  
Eine Zeile EllipticalArcTo enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *X* -Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die *X* -Koordinate des Kontrollpunkts des Bogens; ein Punkt auf dem Bogen. Kontrollpunkts ist die beste in der Mitte zwischen dem ersten und letzten Scheitelpunkt des Bogens. Andernfalls kann Bogens extrem große anwachsen, um passieren Kontrollpunkts weitergibt.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Kontrollpunkts des Bogens.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Der Winkel der Größenachse des Bogens relativ zu der *X* -Achse des übergeordneten Objekts.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.  <br/> |
   

