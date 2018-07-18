---
title: RelEllipticalArcTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: Enthält X - und y - Koordinate des Endpunkts der eines elliptischen Bogens relativ zu der Breite des Shapes und Höhe, X- und y-Koordinaten der Kontrollpunkte des Bogens relativ zur Höhe und Breite des Shapes Winkel von X-Achse zu großen Achse der Ellipse und das Verhältnis zwischen t Haupt- und Hilfsintervalle Achse der Ellipse IE
ms.openlocfilehash: 417a2a92bc5c94f9620c7c6f1081ba81d93aa890
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797808"
---
# <a name="relellipticalarcto-row-geometry-section"></a>RelEllipticalArcTo Row (Geometry Section)

Enthält die *X* - und *y* - Koordinate des Endpunkts der eines elliptischen Bogens relativ zu der Breite des Shapes und Höhe, *X* - und *y* -Koordinaten der Kontrollpunkte des Bogens relativ zur Höhe und Breite des Shapes Winkel von der *x*   -Achse zu großen Achse der Ellipse und das Verhältnis zwischen der Ellipse Haupt- und Hilfsintervalle Achsen. 
  
> [!NOTE]
> Eine Zeile **RelEllipticalArcTo** kann nur in den Dateiformaten .vsdx, .vsdm, .vstx, .vstm, .vssx und .vssm beibehalten werden. Wenn eine Datei in das Visio 2003-2010-Formate gespeichert wird, wird die Zeile **RelEllipticalArcTo** in [eine Zeile EllipticalArcTo](ellipticalarcto-row-geometry-section.md) konvertiert. 
  
Eine Zeile **RelEllipticalArcTo** enthält folgende Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *X* -Koordinate des Endscheitelpunkts eines Bogens relativ zu der Breite der Form.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Endscheitelpunkts eines Bogens relativ zur Höhe des Shapes.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die *X* -Koordinate des Kontrollpunkts des Bogens, relativ zur Breite des Shapes; ein Punkt auf dem Bogen. Kontrollpunkts ist die beste in der Mitte zwischen dem ersten und letzten Scheitelpunkt des Bogens. Andernfalls kann Bogens extrem große anwachsen, um passieren Kontrollpunkts weitergibt.  <br/> |
|[B](b-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Kontrollpunkts des Bogens, relativ zu der Breite des Shapes.  <br/> |
|[C](c-cell-geometry-section.md) <br/> |Der Winkel der Größenachse des Bogens relativ zu der *X* -Achse des übergeordneten Objekts.  <br/> |
|[D](d-cell-geometry-section.md) <br/> |Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte in der Zeile **RelEllipticalArcTo** entsprechen Werten in einer [EllipticalArcTo](ellipticalarcto-row-geometry-section.md) -Zeile, die die Breite und Höhe des Shapes multipliziert. Beispiel: ein **RelEllipticalArcTo** Zeile, in dem die Zellen **X**, **Y**, **A**, **B**, **C**und **D** die Werte aufweisen, 1, 1, 1,5, 0,5, 15 deg und 1,5 (entsprechend) können ersetzt werden mit einer **EllipticalArcTo** -Zeile mit Die Zellformeln `Width*1`, `Height*1'`, `Width*1.5`, `Height*0.5`, 15 deg und 1,5 (entsprechend).
  

