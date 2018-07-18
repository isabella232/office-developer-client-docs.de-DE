---
title: RelMoveTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Enthält die X - und y - Koordinaten des ersten Scheitelpunkts eines Shapes oder die X- und y-Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke in einem Pfad, relativ zur Höhe und Breite der Form.
ms.openlocfilehash: 77b3e731bfd1f35abe34ffbf3155b57133e56412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797821"
---
# <a name="relmoveto-row-geometry-section"></a>RelMoveTo Row (Geometry Section)

Enthält die *X* - und *y* - Koordinaten des ersten Scheitelpunkts eines Shapes oder die *X* - und *y* -Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke in einem Pfad, relativ zur Höhe und Breite der Form. 
  
> [!NOTE]
> Eine Zeile **RelMoveTo** kann nur in den Dateiformaten .vsdx, .vsdm, .vstx, .vstm, .vssx und .vssm beibehalten werden. Wenn eine Datei in das Visio 2003-2010-Formate gespeichert wird, wird die Zeile **RelMoveTo** in eine Zeile [MoveTo](moveto-row-geometry-section.md) konvertiert. 
  
Eine Zeile **RelMoveTo** enthält folgende Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Wenn die **RelMoveTo** Zeile der ersten Zeile im Abschnitt ist, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts eines Shapes relativ zu der Breite der Form. Wenn die Zeile **RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Wenn die **RelMoveTo** Zeile der ersten Zeile im Abschnitt ist, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts eines Shapes. Wenn die Zeile **RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte in der Zeile **RelMoveTo** entsprechen Werten in einer Zeile [MoveTo](moveto-row-geometry-section.md) , die die Breite und Höhe des Shapes multipliziert werden. Beispiel: eine Zeile **RelMoveTo** , in denen der Wert der Zelle **X** ist "0" und der Wert der Zelle **Y** ist "0,5" konnte mit **MoveTo** -Zeile, in dem der Wert der Zelle **X** die Formel lautet, ersetzt werden "Breite*0" und die Zelle **Y** ist die Formel "Höhe*0,5." 
  
Die **RelMoveTo** Zeile enthält, die *X* - und *y* -Koordinaten des ersten Scheitelpunkts für das Shape, wenn die Zeile MoveTo die erste Zeile im Abschnitt ist. In der Regel ist dies dem ersten Scheitelpunkt und es entspricht nicht notwendigerweise auf den Anfangspunkt eines 1D-Shapes Shapes beim Zeichnen des Shapes platziert. 
  
Ein Abschnitt **Geometry** muss mit einem **MoveTo** oder eine Zeile **RelMoveTo** beginnen, aber Sie können der **RelMoveTo** Zeile und die Zeile **MoveTo** auch verwenden, um eine Lücke im Verlauf des Pfads einer Form, relativ zur Breite und Höhe des Shapes darzustellen. Wenn der Pfad verwendet wird, um die Grenze eines ausgefüllten Bereichs zu definieren, wird die Lücke als eines geraden Linienabschnitts interpretiert. Um solche eine Lücke einfügen möchten, fügen Sie eine Zeile zwischen zwei Zeilen, und ändern Sie den Zeilentyp in **RelMoveTo**. Wenn die Zeile **RelMoveTo** zwischen zwei Zeilen befindet, enthält die *X* - und *y* -Koordinaten des ersten Scheitelpunkts des Linie nach der Unterbrechung im Pfad des Shapes. 
  

