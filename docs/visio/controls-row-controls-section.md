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
description: Enthält Zellen, die die x-und y-Koordinaten und das Verhalten der einzelnen Steuerelemente definieren, die für ein Shape definiert sind. Ein Shape enthält eine Zeile mit Steuerelementen für jeden Steuerpunkt.
ms.openlocfilehash: dd5a96fe297cb62996ac2ab4d2974b8d1ae61a14
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282957"
---
# <a name="controls-row-controls-section"></a>Zeile "Controls" (Abschnitt "Controls")

Enthält Zellen, die die *x* -und *y* -Koordinaten und das Verhalten der einzelnen Steuerelemente definieren, die für ein Shape definiert sind. Ein Shape enthält eine Zeile mit Steuerelementen für jeden Steuerpunkt. 
  
Steuerelemente Zeilen sind benannte Steuerelemente. *Name* und enthalten die folgenden Zellen. Weitere Informationen finden Sie in den Themen zu bestimmten Zellen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Stellt die *x* -Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Stellt die *y* -Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt.  <br/> |
|[X-Dynamik](x-dynamics-cell-controls-section.md) <br/> |Stellt die *x* -Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar.  <br/> |
|[Y-Dynamik](y-dynamics-cell-controls-section.md) <br/> |Stellt die *y* -Koordinate für den Verankerungspunkt eines Steuerelements in lokalen Koordinaten dar.  <br/> |
|[X-Verhalten](x-behavior-cell-controls-section.md) <br/> |Steuert die Art des Verhaltens, das die *x* -Koordinate des Steuerpunkts zeigt, nachdem der Ziehpunkt verschoben wurde.  <br/> |
|[Y-Verhalten](y-behavior-cell-controls-section.md) <br/> |Steuert die Art des Verhaltens, die die *y* -Koordinate des Steuerpunkts zeigt, nachdem der Ziehpunkt verschoben wurde.  <br/> |
|[Kleben möglich](can-glue-cell-controls-section.md) <br/> |Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.  <br/> |
|[Tipp](tip-cell-controls-section.md) <br/> |Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn der Mauszeiger über dem Steuerpunkt eines Shapes platziert wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

 Sie können so viele Steuerelemente hinzufügen.  *benennen* Sie Zeilen, die Sie benötigen, und weisen Sie den Zeilen aussagekräftige Namen zu. Um einem vorhandenen Steuerelement Steuerpunkte hinzuzufügen, klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie dann im Kontextmenü auf **Zeile einfügen** . 
  
Sie können auf diese Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. Zuweisen von aussagekräftigen Namen zu Steuerelementen. *Name* rows, klicken Sie auf die Zeile, und geben Sie dann *Custom* ein, beispielsweise, um den Zeilennamen Controls. Custom zu erstellen. Sie können dann mithilfe von Controls. Custom. X auf die Zelle X verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

