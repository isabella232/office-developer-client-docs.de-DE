---
title: Zeile "RelLineTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Enthält x- und y-Koordinaten des Endscheitelpunkts eines geraden Liniensegments relativ zur Breite und Höhe eines Shapes.
ms.openlocfilehash: 24f9f5c7de5b71f451f4d2e907d56516cc3b3c25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570176"
---
# <a name="rellineto-row-geometry-section"></a>Zeile "RelLineTo" (Abschnitt "Geometry")

Enthält  *x-*  und  *y-Koordinaten*  des Endscheitelpunkts eines geraden Liniensegments relativ zur Breite und Höhe eines Shapes. 
  
> [!NOTE]
> Eine **RelLineTo-Zeile** kann nur in den Dateiformaten .vsdx, .vsdm, .vstx, .vstm, .vssx und .vssm beibehalten werden. Wenn eine Datei in den Formaten Visio 2003-2010 gespeichert wird, wird die **Zeile "RelLineTo"** in eine [Zeile "LineTo"](lineto-row-geometry-section.md) konvertiert. 
  
Eine **Zeile RelLineTo** enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die  X-Koordinate des Endscheitelpunkts eines geraden Liniensegments relativ zur Breite des Shapes.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die  y-Koordinate des Endscheitelpunkts eines geraden Liniensegments relativ zur Höhe des Shapes.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Werte in der **Zeile "RelLineTo"** entsprechen Werten in einer [Zeile "LineTo",](lineto-row-geometry-section.md) die mit der Breite und Höhe der Form multipliziert werden. Beispiel: Eine **RelLineTo-Zeile,** bei der der Wert der **X-Zelle** "0" und der Wert der **Y-Zelle** "0,5" lautet, kann durch die **Zeile "LineTo"** ersetzt werden, wobei der Wert der **X-Zelle** die Formel "Width *0" und die **Zelle Y** die Formel "Height* 0,5" ist. 
  

