---
title: Zeile "RelMoveTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Enthält die x-und y-Koordinaten des ersten Scheitelpunkts einer Form oder die x-und y-Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad, relativ zur Höhe und Breite der Form.
ms.openlocfilehash: 488945dbeeea177514770da57b5f26ac947053a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319922"
---
# <a name="relmoveto-row-geometry-section"></a>Zeile "RelMoveTo" (Abschnitt "Geometry")

Enthält die *x* -und *y* -Koordinaten des ersten Scheitelpunkts einer Form oder die *x* -und *y* -Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad, relativ zur Höhe und Breite der Form. 
  
> [!NOTE]
> Eine **RelMoveTo** -Zeile kann nur im. vsdx-, vsdm-, vstx-, VSTM-, vssx-und VSSM-Dateiformat gespeichert werden. Wenn eine Datei im Visio 2003-2010-Format gespeichert wird, wird die **RelMoveTo** -Zeile in eine [MoveTo](moveto-row-geometry-section.md) -Zeile konvertiert. 
  
Eine **RelMoveTo** -Zeile enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Wenn die Zeile **RelMoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts einer Form relativ zur Breite der Form dar. Wenn die **RelMoveTo** -Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Wenn die **RelMoveTo** -Zeile die erste Zeile im Abschnitt ist, stellt die Zelle y die *y* -Koordinate des ersten Scheitelpunkts einer Form dar. Wenn die **RelMoveTo** -Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle y die *y* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte in der **RelMoveTo** -Zeile sind äquivalent zu Werten in einer [MoveTo](moveto-row-geometry-section.md) -Zeile, die mit der Breite und Höhe der Form multipliziert werden. Beispiel: eine **RelMoveTo** Zeile, bei der der Wert der Zelle **x** "0" ist und der Wert der zelle **y** lautet "0,5", konnte durch **MoveTo** Zeile ersetzt werden, wobei der Wert der Zelle **x** die Formel "Breite*0" ist und die **y** -Zelle die Formel "Height*0,5." 
  
Die Zeile **RelMoveTo** enthält die *x* -und *y* -Koordinaten des ersten Scheitelpunkts für das Shape, wenn die MoveTo-Zeile die erste Zeile im Abschnitt ist. In der Regel ist dies der erste Scheitelpunkt, der beim Zeichnen des Shapes festgelegt wurde, und es entspricht nicht unbedingt dem Anfangszeitpunkt eines 1D-Shapes. 
  
Ein **Geometry** -Abschnitt muss mit einer **MoveTo** -oder einer **RelMoveTo** -Zeile beginnen, aber Sie können auch die Zeile **RelMoveTo** und **MoveTo** verwenden, um eine Lücke in der Kontur des Pfads eines Shapes relativ zur Breite und Höhe der Form darzustellen. Wenn jedoch der Pfad verwendet wird, um die Grenze eines ausgefüllten Bereichs zu definieren, wird dieser Abstand als gerade Linie interpretiert. Um eine solche Lücke einzufügen, fügen Sie eine Zeile zwischen zwei Zeilen ein, und ändern Sie den Zeilentyp in **RelMoveTo**. Wenn sich die **RelMoveTo** -Zeile zwischen zwei Zeilen befindet, enthält Sie die *x* -und *y* -Koordinaten des ersten Scheitelpunkts der Linie nach der Unterbrechung im Pfad des Shapes. 
  

