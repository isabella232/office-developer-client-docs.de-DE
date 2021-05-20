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
description: Enthält die x- und y-Koordinaten und den Bogen eines kreisförmigen Bogens.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430042"
---
# <a name="arcto-row-geometry-section"></a>Zeile "ArcTo" (Abschnitt "Geometry")

Enthält die  *x-*  und  *y-Koordinaten*  und den Bogen eines kreisförmigen Bogens. 
  
Eine Zeile ArcTo enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die  x-Koordinate des endenden Scheitelpunkts eines Bogens.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die  y-Koordinate des endenden Scheitelpunkts eines Bogens.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die Entfernung zwischen dem Mittelpunkt des Bogens und dem Mittelpunkt seiner Sehne.  <br/> |
   
## <a name="remarks"></a>Hinweise

In Visio gezeichnete Bögen sind elliptisch, auch wenn sie auf einem Kreis basieren. Standardmäßig werden gezeichnete Bögen durch eine Zeile EllipticalArcTo in einem ShapeSheet-Fenster dargestellt. Wenn Sie eine Zeile ArcTo in einem ShapeSheet-Fenster anzeigen möchten, müssen Sie einen Bogen zeichnen und dann den Zeilentyp EllipticalArcTo in den Zeilentyp ArcTo ändern, wodurch Sie einen elliptischen Bogen letztendlich in einen kreisförmigen Bogen ändern.
  
Klicken Sie mit der rechten Maustaste auf eine Zeile, um den Zeilentyp zu ändern, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**. 
  

