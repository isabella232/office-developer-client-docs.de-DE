---
title: Zeile "MoveTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
ms.localizationpriority: medium
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Enthält die x- und y-Koordinaten des ersten Scheitelpunkts eines Shapes oder stellt die x- und y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad dar.
ms.openlocfilehash: 77328e6a8b08099d42703034beb32c3835e2cb8c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573880"
---
# <a name="moveto-row-geometry-section"></a>Zeile "MoveTo" (Abschnitt "Geometry")

Enthält die  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts eines Shapes oder stellt die  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts nach einem Umbruch in einem Pfad dar. 
  
Eine **MoveTo-Zeile** enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Wenn die **Zeile MoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle X die X-Koordinate des ersten Scheitelpunkts eines Shapes dar.  Wenn die **Zeile MoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die X-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.   <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Wenn die **Zeile MoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle Y die Y-Koordinate des ersten Scheitelpunkts eines Shapes dar.  Wenn die **Zeile MoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die Y-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.   <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **Zeile MoveTo** enthält die  *X-*  und  *Y-Koordinaten*  des ersten Scheitelpunkts für das Shape, wenn die **Zeile MoveTo** die erste Zeile im Abschnitt ist. In der Regel ist dies der erste Scheitelpunkt, der beim Zeichnen der Form platziert wurde, und entspricht nicht notwendigerweise dem Anfangspunkt eines 1D-Shapes. 
  
Ein Geometrieabschnitt muss entweder mit einer **Zeile "RelMoveTo"** oder einer **Zeile "MoveTo"** beginnen. Sie können jedoch auch die Zeilen **"MoveTo"** und **"RelMoveTo"** verwenden, um eine Lücke im Strich des Pfads eines Shapes darzustellen. Wenn der Pfad jedoch zum Definieren der Grenze eines gefüllten Bereichs verwendet wird, wird diese Lücke als gerades Liniensegment interpretiert. Um eine solche Lücke einzufügen, fügen Sie eine Zeile zwischen zwei Zeilen ein, und ändern Sie den Zeilentyp in **MoveTo**. Wenn sich die **Zeile MoveTo** zwischen zwei Zeilen befindet, enthält sie die  *X-*  und  *Y-Koordinaten*  des ersten Scheitelpunkts der Linie nach dem Umbruch im Pfad des Shapes. 
  

