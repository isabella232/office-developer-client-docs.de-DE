---
title: Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Enthält x- und y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe des Shapes, x- und y-Koordinaten der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, zum Winkel von der x-Achse zur Hauptachse der Ellipse und zum Verhältnis zwischen der Haupt- und Hilfsachse der Ellipse.
ms.openlocfilehash: ce97c531e199acc74c0b3581dcf24e72dbf2899b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607822"
---
# <a name="relellipticalarcto-row-geometry-section"></a>Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")

Enthält  *x-*  und  *y-Koordinaten*  des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe des Shapes,  *x-*  und  *y-Koordinaten*  der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, zum Winkel von der  *x-Achse*  zur Hauptachse der Ellipse und zum Verhältnis zwischen der Haupt- und Hilfsachse der Ellipse. 
  
> [!NOTE]
> Eine **Zeile "RelEllipticalArcTo"** kann nur in den Dateiformaten ".vsdx", ".vsdm", ".vstx", ".vstm", ".vssx" und ".vssm" beibehalten werden. Wenn eine Datei in den Formaten Visio 2003-2010 gespeichert wird, wird die Zeile **"RelEllipticalArcTo"** in eine [EllipticalArcTo-Zeile](ellipticalarcto-row-geometry-section.md) konvertiert. 
  
Eine **Zeile RelEllipticalArcTo** enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die  X-Koordinate des Endscheitelpunkts in einem Bogen relativ zur Breite des Shapes.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die  y-Koordinate des Endscheitelpunkts in einem Bogen relativ zur Höhe des Shapes.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die  X-Koordinate des Kontrollpunkts des Bogens relativ zur Breite des Shapes; ein Punkt auf dem Bogen. Der Kontrollpunkt befindet sich am besten etwa in der Mitte zwischen den Anfangs- und Endscheitelpunkten des Bogens. Andernfalls kann der Bogen zu einer extrem großen Größe werden, um den Kontrollpunkt zu durchlaufen, was zu unvorhersehbaren Ergebnissen führt.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Die  y-Koordinate des Kontrollpunkts eines Bogens relativ zur Breite des Shapes.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Der Winkel der Hauptachse eines Bogens relativ zur  *X-Achse*  des übergeordneten Bereichs.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Werte in der Zeile **"RelEllipticalArcTo"** entsprechen den Werten in einer [EllipticalArcTo-Zeile,](ellipticalarcto-row-geometry-section.md) multipliziert mit der Breite und Höhe der Form. Beispiel: Eine **RelEllipticalArcTo-Zeile,** in der die Zellen **X,** **Y,** **A,** **B,** **C** und **D** die Werte 1, 1, 1,5, 0,5, 15 deg und 1,5 (jeweils) aufweisen, können durch eine **Zeile EllipticalArcTo** mit den Zellformeln  `Width*1` , , , ,  `Height*1'`  `Width*1.5`  `Height*0.5` 15 deg und 1,5 (jeweils) ersetzt werden.
  

