---
title: Zeile "Controls" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1024624
localization_priority: Normal
ms.assetid: a57bdcd9-566b-5054-7458-7d84cbb78d23
description: Enthält Zellen, die definieren, die X- und y-Koordinaten und das Verhalten der einzelnen Steuerpunkt eines Shapes definiert. Ein Shape enthält für jeden Kontrollpunkt eine Zeile mit Steuerelementen.
ms.openlocfilehash: ed1d57fce6d413b9eb7f5d119264bc2bfa968222
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796740"
---
# <a name="controls-row-controls-section"></a>Controls Row (Controls Section)

Enthält Zellen, die definieren, die *X* - und *y* -Koordinaten und das Verhalten der einzelnen Steuerpunkt eines Shapes definiert. Ein Shape enthält für jeden Kontrollpunkt eine Zeile mit Steuerelementen. 
  
Controls-Zeilen heißen Steuerelemente. *Name* und enthält folgenden Zellen. Weitere Informationen finden Sie unter die folgenden Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Stellt die *X* -Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Stellt die *y* -Koordinate, die die Position des Steuerpunkts in lokalen Koordinaten des Shapes anzeigt.  <br/> |
|[X Dynamics](x-dynamics-cell-controls-section.md) <br/> |Stellt die *X* -Koordinate für den Verankerungspunkt eines Steuerpunkts, in lokalen Koordinaten dar.  <br/> |
|[Y Dynamics](y-dynamics-cell-controls-section.md) <br/> |Stellt die *y* -Koordinate für den Verankerungspunkt eines Steuerpunkts, in lokalen Koordinaten dar.  <br/> |
|[X-Verhalten](x-behavior-cell-controls-section.md) <br/> |Steuert das Verhalten, das die *X* -Koordinate der Steuerpunkt Steuerpunkts zeigt, wenn dieser verschoben wird.  <br/> |
|[Y-Verhalten](y-behavior-cell-controls-section.md) <br/> |Steuert das Verhalten der *y* -Koordinate der Steuerpunkt Steuerpunkts zeigt, wenn dieser verschoben wird.  <br/> |
|[Zelle Can Glue](can-glue-cell-controls-section.md) <br/> |Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.  <br/> |
|[Tipp](tip-cell-controls-section.md) <br/> |Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn der Mauszeiger über dem Steuerpunkt eines Shapes platziert wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

 Sie können beliebig viele Steuerelemente hinzufügen.  *Namen* Zeilen wie Sie benötigen, den Zeilen aussagekräftige Namen zuweisen und Zellenwerte festlegen. Um einem vorhandenen Abschnitt Controls Kontrollpunkte hinzuzufügen, mit der rechten Maustaste in einer Zeile, und klicken Sie im Kontextmenü auf **Zeile einfügen** . 
  
Sie können diese Zellen anhand ihrer Zeilennamen verweisen, die in einem ShapeSheet-Fenster als roter Text angezeigt. Steuerelemente aussagekräftige Namen zuzuweisen. *Namen* Zeilen, klicken Sie auf die Zeile, und geben Sie *benutzerdefinierte* , z. B., um den Zeilennamen Controls.Custom zu erstellen. Sie können dann die Zelle X mit Controls.Custom.X verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

