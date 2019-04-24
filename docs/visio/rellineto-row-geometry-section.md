---
title: Zeile "RelLineTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Enthält die x-und y-Koordinaten des Endpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe eines Shapes.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320069"
---
# <a name="rellineto-row-geometry-section"></a>Zeile "RelLineTo" (Abschnitt "Geometry")

Enthält die *x* -und *y* -Koordinaten des Endpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe eines Shapes. 
  
> [!NOTE]
> Eine **RelLineTo** -Zeile kann nur im. vsdx-, vsdm-, vstx-, VSTM-, vssx-und VSSM-Dateiformat gespeichert werden. Wenn eine Datei im Visio 2003-2010-Format gespeichert wird, wird die **RelLineTo** -Zeile in eine [LineTo](lineto-row-geometry-section.md) -Zeile konvertiert. 
  
Eine **RelLineTo** -Zeile enthält die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *x* -Koordinate des Endpunkts eines geraden Linienabschnitts relativ zur Breite der Form.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Endpunkts eines geraden Linienabschnitts relativ zur Höhe der Form.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte in der **RelLineTo** -Zeile sind äquivalent zu Werten in einer [LineTo](lineto-row-geometry-section.md) -Zeile, die mit der Breite und Höhe der Form multipliziert werden. Beispiel: eine **RelLineTo** Zeile, bei der der Wert der Zelle **x** "0" ist und der Wert der Zelle **y** "0,5" ist, kann durch **LineTo** Zeile ersetzt werden, wobei der Wert der Zelle **x** die Formel "Breite*0" ist und die **y** -Zelle die Formel "Height*0,5." 
  

