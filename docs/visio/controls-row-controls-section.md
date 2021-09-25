---
title: Zeile "Controls" (Abschnitt "Controls")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1024624
ms.localizationpriority: medium
ms.assetid: a57bdcd9-566b-5054-7458-7d84cbb78d23
description: Enthält Zellen, die die x- und y-Koordinaten und das Verhalten jedes für ein Shape definierten Steuerpunkts definieren. Ein Shape enthält eine Steuerelementzeile für jeden Steuerpunkt.
ms.openlocfilehash: d839eb8818263ae630895cc4e3bee0c8a2ec99cb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582946"
---
# <a name="controls-row-controls-section"></a>Zeile "Controls" (Abschnitt "Controls")

Enthält Zellen, die die  *x-*  und  *y-Koordinaten*  und das Verhalten jedes für ein Shape definierten Steuerpunkts definieren. Ein Shape enthält eine Steuerelementzeile für jeden Steuerpunkt. 
  
Steuerelementzeilen haben den Namen "Steuerelemente". *die*  folgenden Zellen benennen und enthalten. Weitere Informationen finden Sie in den spezifischen Zellthemen. 
  
|**Cell**|**Beschreibung**|
|:-----|:-----|
|[x](x-cell-controls-section.md) <br/> |Stellt  die x-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt.  <br/> |
|[y](y-cell-controls-section.md) <br/> |Stellt  die y-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten angibt.  <br/> |
|[X-Dynamik](x-dynamics-cell-controls-section.md) <br/> |Stellt  die X-Koordinate für den Ankerpunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |
|[Y-Dynamik](y-dynamics-cell-controls-section.md) <br/> |Stellt  die y-Koordinate für den Ankerpunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |
|[X-Verhalten](x-behavior-cell-controls-section.md) <br/> |Steuert die Art  des Verhaltens, das die X-Koordinate des Steuerpunkts nach dem Verschieben des Ziehpunkts zeigt.  <br/> |
|[Y-Verhalten](y-behavior-cell-controls-section.md) <br/> |Steuert die Art  des Verhaltens, das die y-Koordinate des Steuerpunkts nach dem Verschieben des Ziehpunkts zeigt.  <br/> |
|[Kleben möglich](can-glue-cell-controls-section.md) <br/> |Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.  <br/> |
|[Tipp](tip-cell-controls-section.md) <br/> |Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn der Mauszeiger über dem Steuerpunkt eines Shapes platziert wird.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 Sie können so viele Steuerelemente hinzufügen.  *Benennen*  Sie Zeilen nach Bedarf, weisen Sie den Zeilen aussagekräftige Namen zu, und legen Sie Zellwerte fest. Klicken Sie mit der rechten Maustaste auf eine Zeile, und klicken Sie im Kontextmenü auf **"Zeile einfügen",** um einem vorhandenen Steuerelementabschnitt Steuerpunkte hinzuzufügen. 
  
Sie können auf diese Zellen anhand ihres Zeilennamens verweisen, der in einem ShapeSheet-Fenster in rotem Text angezeigt wird. So weisen Sie Steuerelementen aussagekräftige Namen zu. *namen*  rows, click the row and then type  *Custom*  , for example, to create the row name Controls.Custom. Anschließend können Sie mithilfe von Controls.Custom.X auf die Zelle "X" verweisen. 
  
Der eingegebene Zeilenname muss innerhalb des Abschnitts eindeutig sein.
  

