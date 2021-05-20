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
description: Enthält Zellen, die die x- und y-Koordinaten und das Verhalten jedes für ein Shape definierten Steuerelementhandpunkts definieren. Ein Shape enthält eine Controls-Zeile für jedes Steuerelementhandle.
ms.openlocfilehash: dd5a96fe297cb62996ac2ab4d2974b8d1ae61a14
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438190"
---
# <a name="controls-row-controls-section"></a>Zeile "Controls" (Abschnitt "Controls")

Enthält Zellen, die die  *x-*  und  *y-Koordinaten*  und das Verhalten jedes für ein Shape definierten Steuerelementhandpunkts definieren. Ein Shape enthält eine Controls-Zeile für jedes Steuerelementhandle. 
  
Steuerelementzeilen heißen Steuerelemente. *namen*  und die folgenden Zellen enthalten. Weitere Informationen finden Sie in den spezifischen Zellthemen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.  <br/> |
|[X-Dynamik](x-dynamics-cell-controls-section.md) <br/> |Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.  <br/> |
|[Y-Dynamik](y-dynamics-cell-controls-section.md) <br/> |Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.  <br/> |
|[X-Verhalten](x-behavior-cell-controls-section.md) <br/> |Steuert die Art  des Verhaltens, das die x-Koordinate des Steuerelementhandles nach dem Verschoben des Handles zeigt.  <br/> |
|[Y-Verhalten](y-behavior-cell-controls-section.md) <br/> |Steuert die Art des Verhaltens, das die y-Koordinate des Steuerelementhandles nach dem Verschoben des Handles zeigt.   <br/> |
|[Kleben möglich](can-glue-cell-controls-section.md) <br/> |Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.  <br/> |
|[Tipp](tip-cell-controls-section.md) <br/> |Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn der Mauszeiger über dem Steuerpunkt eines Shapes platziert wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

 Sie können so viele Steuerelemente hinzufügen.  *name*  rows as you need, assign meaningful names to the rows, and set cell values. Klicken Sie zum Hinzufügen von Steuerelementhandles zu einem vorhandenen Abschnitt Steuerelemente mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü **auf** Zeile einfügen. 
  
Sie können auf diese Zellen durch ihren Zeilennamen verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. So weisen Sie Steuerelementen aussagekräftige Namen zu. *name*  rows, click the row and then type  *Custom*  , for example, to create the row name Controls.Custom. Anschließend können Sie mithilfe von Controls.Custom.X auf die Zelle X verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

