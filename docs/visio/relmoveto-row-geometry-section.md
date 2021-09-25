---
title: Zeile "RelMoveTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Enthält die x- und y-Koordinaten des ersten Scheitelpunkts eines Shapes oder die X- und y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite des Shapes.
ms.openlocfilehash: 1878a8663ef72fbb5f248a160c0abd0d20458baa
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598388"
---
# <a name="relmoveto-row-geometry-section"></a>Zeile "RelMoveTo" (Abschnitt "Geometry")

Enthält die  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts eines Shapes oder die  *X-*  und  *y-Koordinaten*  des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite des Shapes. 
  
> [!NOTE]
> Eine **RelMoveTo-Zeile** kann nur in den Dateiformaten ".vsdx", ".vsdm", ".vstx", ".vstm", ".vssx" und ".vssm" beibehalten werden. Wenn eine Datei in den Formaten Visio 2003-2010 gespeichert wird, wird die **Zeile "RelMoveTo"** in eine [MoveTo-Zeile](moveto-row-geometry-section.md) konvertiert. 
  
Eine **Zeile RelMoveTo** enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Wenn die **Zeile RelMoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle X die X-Koordinate des ersten Scheitelpunkts eines Shapes relativ zur Breite des Shapes dar.  Wenn die **Zeile RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die X-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.   <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Wenn die **Zeile RelMoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle Y die Y-Koordinate des ersten Scheitelpunkts eines Shapes dar.  Wenn die **Zeile RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die Y-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.   <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Werte in der **Zeile RelMoveTo** entsprechen Werten in einer [MoveTo-Zeile,](moveto-row-geometry-section.md) die mit der Breite und Höhe des Shapes multipliziert werden. Beispiel: Eine **RelMoveTo-Zeile,** bei der der Wert der **X-Zelle** "0" und der Wert der **Zelle Y** "0,5" lautet, kann durch die **Zeile "MoveTo"** ersetzt werden, wobei der Wert der **X-Zelle** die Formel "Width *0" und die **Zelle Y** die Formel "Height* 0.5" ist. 
  
Die **Zeile RelMoveTo** enthält die  *X-*  und  *Y-Koordinaten*  des ersten Scheitelpunkts für das Shape, wenn die Zeile MoveTo die erste Zeile im Abschnitt ist. In der Regel ist dies der erste Scheitelpunkt, der beim Zeichnen der Form platziert wurde, und entspricht nicht notwendigerweise dem Anfangspunkt eines 1D-Shapes. 
  
Ein **Geometry-Abschnitt** muss mit einer **Zeile MoveTo** oder RelMoveTo beginnen. Sie können jedoch auch die Zeile **RelMoveTo** und MoveTo verwenden, um einen Abstand im Pfad des Shapes relativ zur Breite und Höhe des Shapes darzustellen.   Wenn der Pfad jedoch zum Definieren der Grenze eines gefüllten Bereichs verwendet wird, wird diese Lücke als gerades Liniensegment interpretiert. Um eine solche Lücke einzufügen, fügen Sie eine Zeile zwischen zwei Zeilen ein, und ändern Sie den Zeilentyp in **RelMoveTo**. Wenn sich die **Zeile RelMoveTo** zwischen zwei Zeilen befindet, enthält sie die  *X-*  und  *Y-Koordinaten*  des ersten Scheitelpunkts der Linie nach dem Umbruch im Pfad des Shapes. 
  

