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
description: Enthält die x-und y-Koordinaten des ersten Scheitelpunkts einer Form oder stellt die x-und y-Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad dar.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283858"
---
# <a name="moveto-row-geometry-section"></a>Zeile "MoveTo" (Abschnitt "Geometry")

Enthält die *x* -und *y* -Koordinaten des ersten Scheitelpunkts einer Form oder stellt die *x* -und *y* -Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad dar. 
  
Eine **MoveTo** -Zeile enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Wenn die **MoveTo** -Zeile die erste Zeile im Abschnitt ist, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts einer Form dar. Wenn die **MoveTo** -Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Wenn die **MoveTo** -Zeile die erste Zeile im Abschnitt ist, stellt die Zelle y die *y* -Koordinate des ersten Scheitelpunkts einer Form dar. Wenn die **MoveTo** -Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle y die *y* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Zeile **MoveTo** enthält die *x* -und *y* -Koordinaten des ersten Scheitelpunkts für das Shape, wenn die **MoveTo** -Zeile die erste Zeile im Abschnitt ist. In der Regel ist dies der erste Scheitelpunkt, der beim Zeichnen des Shapes festgelegt wurde, und es entspricht nicht unbedingt dem Anfangszeitpunkt eines 1D-Shapes. 
  
Ein Geometry-Abschnitt muss entweder mit einer **RelMoveTo** -oder einer **MoveTo** -Zeile beginnen, aber Sie können auch die **MoveTo** -und **RelMoveTo** -Zeilen verwenden, um eine Lücke beim streicheln des Pfads einer Form darzustellen. Wenn jedoch der Pfad verwendet wird, um die Grenze eines ausgefüllten Bereichs zu definieren, wird dieser Abstand als gerade Linie interpretiert. Um eine solche Lücke einzufügen, fügen Sie eine Zeile zwischen zwei Zeilen ein, und ändern Sie den Zeilentyp in **MoveTo**. Wenn sich die **MoveTo** -Zeile zwischen zwei Zeilen befindet, enthält Sie die *x* -und *y* -Koordinaten des ersten Scheitelpunkts der Linie nach der Unterbrechung im Pfad des Shapes. 
  

