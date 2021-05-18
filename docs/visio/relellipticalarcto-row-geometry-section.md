---
title: RelEllipticalArcTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Enthält x- und y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, x- und y-Koordinaten der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, Winkel von der X-Achse zur Hauptachse der Ellipse und Verhältnis zwischen den Haupt- und Nebenachsen der Ellipse.
ms.openlocfilehash: e38f5f2baf6bb9ade31c2778799a3ece968147f4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409097"
---
# <a name="relellipticalarcto-row-geometry-section"></a>RelEllipticalArcTo Row (Geometry Section)

Enthält  *x-*  und  *y-Koordinaten*  des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form,  *x-*  und  *y-Koordinaten*  der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, Winkel von der  *X-Achse*  zur Hauptachse der Ellipse und Verhältnis zwischen den Haupt- und Nebenachsen der Ellipse. 
  
> [!NOTE]
> Eine **RelEllipticalArcTo-Zeile** kann nur in den Dateiformaten VSDX, VSDM, VSTX, VSTM, VSSX und VSSM beibehalten werden. Wenn eine Datei in den Formaten Visio 2003-2010 gespeichert wird, wird die **Zeile RelEllipticalArcTo** in eine [Zeile EllipticalArcTo](ellipticalarcto-row-geometry-section.md) konvertiert. 
  
Eine **RelEllipticalArcTo-Zeile** enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die  x-Koordinate des endenden Scheitelpunkts in einem Bogen relativ zur Breite der Form.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die  y-Koordinate des endenden Scheitelpunkts in einem Bogen relativ zur Höhe der Form.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die  x-Koordinate des Kontrollpunkts des Bogens relativ zur Breite des Shapes; einen Punkt im Bogen. Der Kontrollpunkt befindet sich am besten ungefähr auf halbem Weg zwischen den Scheitelpunkte am Anfang und Ende des Bogens. Andernfalls kann der Bogen zu einer extremen Größe anwachsen, um den Kontrollpunkt mit unvorhersehbaren Ergebnissen zu passieren.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Die  y-Koordinate des Kontrollpunkts eines Bogens relativ zur Breite des Shapes.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Der Winkel der Hauptachse eines Bogens relativ zur  *x-Achse*  des übergeordneten Bogens.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.  <br/> |
   
## <a name="remarks"></a>Hinweise

Werte in der **Zeile RelEllipticalArcTo** entsprechen Werten in einer [EllipticalArcTo-Zeile,](ellipticalarcto-row-geometry-section.md) multipliziert mit der Breite und Höhe der Form. Beispiel: eine **RelEllipticalArcTo-Zeile,** in der die Zellen **X,** **Y,** **A,** **B,** **C** und **D** die Werte 1, 1, 1,5, 0,5, 15 deg und 1,5 (bzw.) durch eine **EllipticalArcTo-Zeile** mit den Zellformeln  `Width*1` , , , ,  `Height*1'`  `Width*1.5`  `Height*0.5` 15 deg und 1,5 (bzw.) ersetzt werden können.
  

