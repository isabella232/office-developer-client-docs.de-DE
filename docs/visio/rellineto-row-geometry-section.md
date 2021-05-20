---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Enthält x- und y-Koordinaten des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Breite und Höhe eines Shapes.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437161"
---
# <a name="rellineto-row-geometry-section"></a>RelLineTo Row (Geometry Section)

Enthält  *x-*  und  *y-Koordinaten*  des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Breite und Höhe eines Shapes. 
  
> [!NOTE]
> Eine **RelLineTo-Zeile** kann nur in den Dateiformaten VSDX, VSDM, VSTX, VSTM, VSSX und VSSM beibehalten werden. Wenn eine Datei in den Formaten Visio 2003-2010 gespeichert wird, wird die **Zeile RelLineTo** in eine [Zeile LineTo](lineto-row-geometry-section.md) konvertiert. 
  
Eine **RelLineTo-Zeile** enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die  x-Koordinate des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Breite des Shapes.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die  y-Koordinate des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Höhe des Shapes.  <br/> |
   
## <a name="remarks"></a>Hinweise

Werte in der **Zeile RelLineTo** entsprechen Werten in einer [Zeile LineTo,](lineto-row-geometry-section.md) die mit der Breite und Höhe der Form multipliziert werden. Beispiel: Eine **RelLineTo-Zeile,** in der der Wert der **Zelle X** "0" und der Wert der Zelle Y "0,5" ist, kann durch die Zeile **LineTo** ersetzt werden, wobei der Wert der Zelle **X** die Formel "Breite 0" und die *Zelle **Y*** die Formel "Höhe 0,5" ist.  
  

