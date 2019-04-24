---
title: Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Enthält die x-und y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, die x-und y-Koordinaten der Steuerpunkte im Bogen relativ zur Breite und Höhe des Shapes, der Winkel von der x-Achse zur Hauptachse der Ellipse und das Verhältnis zwischen t Haupt-und Nebenachsen der Ellipse.
ms.openlocfilehash: e38f5f2baf6bb9ade31c2778799a3ece968147f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359962"
---
# <a name="relellipticalarcto-row-geometry-section"></a>Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")

Enthält die *x* -und *y* -Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, die *x* -und *y* -Koordinaten der Steuerpunkte im Bogen relativ zur Breite und Höhe des Shapes, Winkel vom *x*   -Achse zur Hauptachse der Ellipse und Verhältnis zwischen Haupt-und Nebenachsen der Ellipse. 
  
> [!NOTE]
> Eine **RelEllipticalArcTo** -Zeile kann nur im. vsdx-, vsdm-, vstx-, VSTM-, vssx-und VSSM-Dateiformat gespeichert werden. Wenn eine Datei im Visio 2003-2010-Format gespeichert wird, wird die **RelEllipticalArcTo** -Zeile in eine [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) -Zeile konvertiert. 
  
Eine **RelEllipticalArcTo** -Zeile enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *x* -Koordinate des Endpunkts auf einem Bogen relativ zur Breite der Form.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Endpunkts auf einem Bogen relativ zur Höhe der Form.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die *x* -Koordinate des Kontrollpunkts des Bogens relativ zur Breite der Form; ein Punkt auf dem Bogen. Der Steuerpunkt befindet sich am besten in der Mitte zwischen dem Anfangs-und Endscheitel des Bogens. Andernfalls kann der Bogen zu einer extremen Größe anwachsen, um den Kontrollpunkt mit unvorhersehbaren Ergebnissen zu durchlaufen.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Steuerpunkts eines Bogens relativ zur Breite der Form.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Der Winkel der Hauptachse eines Bogens relativ zur *x* -Achse des übergeordneten Elements.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte in der **RelEllipticalArcTo** -Zeile sind äquivalent zu Werten in einer [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) -Zeile, multipliziert mit der Breite und Höhe der Form. beispiel: eine **RelEllipticalArcTo** zeile, in der die zellen **X**, **Y**, **a**, **B**, **C**und **D** die werte 1, 1, 1,5, 0,5, 15 deg und 1,5 (beziehungsweise) enthalten, können durch eine **EllipticalArcTo** -zeile mit die zellformeln `Width*1` `Height*1'` `Width*1.5` `Height*0.5`,,,, 15 deg, und 1,5 (beziehungsweise).
  

