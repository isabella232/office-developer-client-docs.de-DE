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
description: Enthält die x- und y-Koordinaten des ersten Scheitelpunkts einer Form oder stellt die x- und y-Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad dar.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429698"
---
# <a name="moveto-row-geometry-section"></a>Zeile "MoveTo" (Abschnitt "Geometry")

Enthält die  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts einer Form oder stellt die  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad dar. 
  
Eine **MoveTo-Zeile** enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Wenn die **MoveTo-Zeile** die erste Zeile im Abschnitt ist, stellt die Zelle X die x-Koordinate des ersten Scheitelpunkts einer Form dar.  Wenn die **MoveTo-Zeile** zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die x-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.   <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Wenn die **MoveTo-Zeile** die erste Zeile im Abschnitt ist, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts einer Form dar.  Wenn die **MoveTo-Zeile** zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.   <br/> |
   
## <a name="remarks"></a>Hinweise

Die MoveTo-Zeile enthält die *x-* und *y-Koordinaten* des ersten Scheitelpunkts für die Form, wenn die **MoveTo-Zeile** die erste Zeile im Abschnitt ist.  In der Regel ist dies der erste Scheitelpunkt, der beim Ziehen der Form platziert wurde, und er entspricht nicht unbedingt dem Anfangspunkt einer 1D-Form. 
  
Ein Geometrieabschnitt muss entweder mit einer **RelMoveTo-** oder einer **MoveTo-Zeile** beginnen, Sie können jedoch auch die **Zeilen MoveTo** und **RelMoveTo** verwenden, um eine Lücke im Streicheln des Pfads eines Shapes zu darstellen. Wenn der Pfad jedoch zum Definieren der Grenze eines gefüllten Bereichs verwendet wird, wird diese Lücke als gerades Segment interpretiert. Fügen Sie zum Einfügen eines solchen Abstands eine Zeile zwischen zwei Zeilen ein, und ändern Sie den Zeilentyp in **MoveTo**. Wenn sich **die MoveTo-Zeile** zwischen zwei Zeilen befindet, enthält sie die  *x-*  und  *y-Koordinaten*  des ersten Scheitelpunkts der Linie nach dem Umbruch im Pfad des Shapes. 
  

