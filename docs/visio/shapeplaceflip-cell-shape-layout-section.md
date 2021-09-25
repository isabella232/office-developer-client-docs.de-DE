---
title: Zelle "ShapePlaceFlip" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
ms.localizationpriority: medium
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Legt fest, wie ein platzierbares Shape auf dem Zeichenblatt gekippt und/oder gedreht wird, wenn Sie Shapes unter Verwendung des Dialogfelds Layout konfigurieren ausrichten. (Klicken Sie dazu auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen.)
ms.openlocfilehash: 4068db4cc4c1eaa96e1b0cd3a1827cbf935dfe9e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622921"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>Zelle "ShapePlaceFlip" (Abschnitt "Shape Layout")

Legt fest, wie ein platzierbares Shape auf dem Zeichenblatt gekippt und/oder gedreht wird, wenn Sie Shapes unter Verwendung des Dialogfelds **Layout konfigurieren** ausrichten. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie dann auf **Weitere Layoutoptionen**.)
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard verwenden:  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |Horizontal kippen.  <br/> |**visLOFlipX** <br/> |
|2  <br/> |Vertikal kippen.  <br/> |**visLOFlipY** <br/> |
|4   <br/> |In 90-Grad-Schritten zwischen 0 und 270 kippen.  <br/> |**visLOFlipRotate** <br/> |
|8   <br/> |Nicht kippen.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert in der Zelle ShapePlaceFlip hilft bei der Ausrichtung eines platzierbaren Shapes in Richtung des nächsten platzierbaren Shapes, mit dem es verbunden ist.
  
Verwenden Sie die Zelle PlaceFlip im Abschnitt Seitenlayout, um dieses Verhalten für  *alle*  Formen auf dem Zeichenblatt festzulegen. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle ShapePlaceFlip anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePlaceFlip  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ShapePlaceFlip anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPlaceFlip** <br/> |
   

