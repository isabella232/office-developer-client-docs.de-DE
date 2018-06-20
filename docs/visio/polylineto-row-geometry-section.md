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
description: Enthält X- und y-Koordinaten des letzten Punkts einer Polylinie und eine Polylinienformel.
ms.openlocfilehash: 56cecb2eeaa1702461b1096fe468974f2f0b1f52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797634"
---
# <a name="polylineto-row-geometry-section"></a>Zeile "PolylineTo" (Abschnitt "Geometry")

Enthält die *X* - und *y* -Koordinaten des letzten Punkts einer Polylinie und eine Polylinienformel. 
  
Eine Zeile PolylineTo enthält folgende Zellen.
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |Die *X* -Koordinate des Endscheitelpunkts einer Polylinie.  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |Die *y* -Koordinate des Endscheitelpunkts einer Polylinie.  <br/> |
|[A](a-cell-geometry-section.md) <br/> |Die Polylinienformel.  <br/> |
   
## <a name="remarks"></a>Hinweise

Zeilen dargestellt als einer Polylinienzeile entsprechen Zeilen, die als Folge von LineTo-Zeilen dargestellt werden, aber eine Polylinienzeile ist effizienter. Sie können eine Zeile PolylineTo in eine Zeile LineTo ändern, sodass Sie auf einfache Weise die Shape-Geometrie anzeigen können. Zu diesem Zweck mit der rechten Maustaste in der Zeile "PolylineTo", und klicken Sie dann im Kontextmenü auf **Zeile erweitern** . 
  
Wenn Sie einen Zeilentyp in eine Zeile PolylineTo ändern, mit der rechten Maustaste in der Zeile, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern** . 
  

