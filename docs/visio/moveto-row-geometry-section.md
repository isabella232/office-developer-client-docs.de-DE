---
title: Zeile "MoveTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Enthält die X- und y - Koordinaten des ersten Scheitelpunkts eines Shapes oder stellt die X - und y-Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke in einem Pfad.
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797532"
---
# <a name="moveto-row-geometry-section"></a>MoveTo Row (Geometry Section)

Enthält die *X* - und *y* - Koordinaten des ersten Scheitelpunkts eines Shapes oder stellt die *X* - und *y* -Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke in einem Pfad. 
  
Eine Zeile **MoveTo** enthält folgende Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Wenn die Zeile **MoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts eines Shapes. Wenn die Zeile **MoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Wenn die Zeile **MoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts eines Shapes. Wenn die Zeile **MoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Zeile **MoveTo** enthält die *X* - und *y* -Koordinaten des ersten Scheitelpunkts für das Shape, wenn die Zeile **MoveTo** die erste Zeile im Abschnitt ist. In der Regel ist dies dem ersten Scheitelpunkt und es entspricht nicht notwendigerweise auf den Anfangspunkt eines 1D-Shapes Shapes beim Zeichnen des Shapes platziert. 
  
Ein Geometrieabschnitt muss mit einem **RelMoveTo** oder eine Zeile **MoveTo** beginnen, aber Sie können auch die Zeilen **MoveTo** und **RelMoveTo** verwenden, um eine Lücke im Verlauf des Shape Pfades darzustellen. Wenn der Pfad verwendet wird, um die Grenze eines ausgefüllten Bereichs zu definieren, wird die Lücke als eines geraden Linienabschnitts interpretiert. Um solche eine Lücke einfügen möchten, fügen Sie eine Zeile zwischen zwei Zeilen, und ändern Sie den Zeilentyp in **MoveTo**. Wenn die Zeile **MoveTo** zwischen zwei Zeilen befindet, enthält die *X* - und *y* -Koordinaten des ersten Scheitelpunkts des Linie nach der Unterbrechung im Pfad des Shapes. 
  

