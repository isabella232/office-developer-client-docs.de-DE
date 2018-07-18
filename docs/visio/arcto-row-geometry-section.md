---
title: Zeile "ArcTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Enthält die X- und y-Koordinaten und die Krümmung eines kreisförmigen Bogens.
ms.openlocfilehash: 77ed0dcaee7ddefa8771d3e890776d4adfcc3b40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796405"
---
# <a name="arcto-row-geometry-section"></a>ArcTo Row (Geometry Section)

Enthält die *X* - und *y* -Koordinaten und die Krümmung eines kreisförmigen Bogens. 
  
Eine Zeile ArcTo enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *X* -Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Endscheitelpunkts eines Bogens.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die Entfernung zwischen dem Mittelpunkt des Bogens und dem Mittelpunkt seiner Sehne.  <br/> |
   
## <a name="remarks"></a>Hinweise

In Visio gezeichnete Bögen sind elliptisch, auch wenn sie auf einem Kreis basieren. Standardmäßig werden gezeichnete Bögen durch eine Zeile EllipticalArcTo in einem ShapeSheet-Fenster dargestellt. Wenn Sie eine Zeile ArcTo in einem ShapeSheet-Fenster anzeigen möchten, müssen Sie einen Bogen zeichnen und dann den Zeilentyp EllipticalArcTo in den Zeilentyp ArcTo ändern, wodurch Sie einen elliptischen Bogen letztendlich in einen kreisförmigen Bogen ändern.
  
Klicken Sie mit der rechten Maustaste auf eine Zeile, um den Zeilentyp zu ändern, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**. 
  

