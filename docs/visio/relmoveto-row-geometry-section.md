---
title: RelMoveTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Enthält die x- und y-Koordinaten des ersten Scheitelpunkts einer Form oder der x- und y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite der Form.
ms.openlocfilehash: 488945dbeeea177514770da57b5f26ac947053a3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414200"
---
# <a name="relmoveto-row-geometry-section"></a>RelMoveTo Row (Geometry Section)

Enthält die  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts einer Form oder der  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite der Form. 
  
> [!NOTE]
> Eine **RelMoveTo-Zeile** kann nur in den Dateiformaten VSDX, VSDM, VSTX, VSTM, VSSX und VSSM beibehalten werden. Wenn eine Datei in den Formaten Visio 2003-2010 gespeichert wird, wird die **Zeile RelMoveTo** in eine [MoveTo-Zeile](moveto-row-geometry-section.md) konvertiert. 
  
Eine **RelMoveTo-Zeile** enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Wenn die **Zeile RelMoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle X die x-Koordinate des ersten Scheitelpunkts einer Form relativ zur Breite der Form dar.  Wenn die **Zeile RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die x-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.   <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Wenn die **Zeile RelMoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts einer Form dar.  Wenn die **Zeile RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.   <br/> |
   
## <a name="remarks"></a>Hinweise

Werte in der **Zeile RelMoveTo** entsprechen Werten in einer [MoveTo-Zeile,](moveto-row-geometry-section.md) die mit der Breite und Höhe der Form multipliziert werden. Beispiel: Eine **RelMoveTo-Zeile,** in der der Wert der **Zelle X** "0" und der Wert der Zelle Y "0,5" ist, könnte durch die Zeile **MoveTo** ersetzt werden, wobei der Wert der Zelle **X** die Formel "Width 0" und die *Zelle **Y*** die Formel "Height 0.5" ist.  
  
Die **Zeile RelMoveTo** enthält die  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts für die Form, wenn die MoveTo-Zeile die erste Zeile im Abschnitt ist. In der Regel ist dies der erste Scheitelpunkt, der beim Ziehen der Form platziert wurde, und er entspricht nicht unbedingt dem Anfangspunkt einer 1D-Form. 
  
Ein **Geometry-Abschnitt** muss mit einer **MoveTo-** oder **einer RelMoveTo-Zeile** beginnen, Sie können jedoch auch die **Zeile RelMoveTo** und **die MoveTo-Zeile** verwenden, um eine Lücke im Streicheln des Pfads eines Shapes relativ zur Breite und Höhe des Shapes zu darstellen. Wenn der Pfad jedoch zum Definieren der Grenze eines gefüllten Bereichs verwendet wird, wird diese Lücke als gerades Segment interpretiert. Fügen Sie zum Einfügen eines solchen Abstands eine Zeile zwischen zwei Zeilen ein, und ändern Sie den Zeilentyp in **RelMoveTo**. Wenn sich **die Zeile RelMoveTo** zwischen zwei Zeilen befindet, enthält sie die  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts der Linie nach dem Umbruch im Pfad des Shapes. 
  

