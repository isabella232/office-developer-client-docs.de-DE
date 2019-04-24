---
title: Zeile "PolylineTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: Enthält die x-und y-Koordinaten des letzten Punkts einer Polylinie und einer Polylinie.
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359829"
---
# <a name="polylineto-row-geometry-section"></a>Zeile "PolylineTo" (Abschnitt "Geometry")

Enthält die *x* -und *y* -Koordinaten des letzten Punkts einer Polylinie und einer Polylinie. 
  
Eine Zeile PolylineTo enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *x* -Koordinate des Endpunkts einer Polylinie.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Endpunkts einer Polylinie.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die Polylinienformel.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Zeilen, die als Polylinie dargestellt werden, sind äquivalent zu Zeilen, die als Sequenz von LineTo-Zeilen dargestellt werden, aber eine Polylinie-Zeile ist effizienter. Sie können eine PolylineTo-Zeile in eine LineTo-Zeile ändern, damit Sie die Form Geometrie leicht erkennen können. Klicken Sie dazu mit der rechten Maustaste auf die PolylineTo-Zeile, und klicken Sie dann im Kontextmenü auf **Zeile erweitern** . 
  
Wenn Sie einen Zeilentyp in eine PolylineTo-Zeile ändern möchten, klicken Sie mit der rechten Maustaste auf die Zeile, und klicken Sie dann im Kontextmenü auf **zeilenTyp ändern** . 
  

