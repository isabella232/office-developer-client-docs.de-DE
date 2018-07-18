---
title: Zelle "ShapePlaceFlip" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253247
localization_priority: Normal
ms.assetid: 40008507-d9e4-9c0e-603f-d5e6da73a94b
description: Legt fest, wie ein platzierbares Shape auf dem Zeichenblatt gekippt und/oder gedreht wird, wenn Sie Shapes unter Verwendung des Dialogfelds Layout konfigurieren ausrichten. (Klicken Sie dazu auf der Registerkarte Entwurf in der Gruppe Layout auf Seite neu anordnen, und klicken Sie dann auf Weitere Layoutoptionen.)
ms.openlocfilehash: 76941b9c50e6f2c68ea9abf54e81dcd18be13a70
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798025"
---
# <a name="shapeplaceflip-cell-shape-layout-section"></a>ShapePlaceFlip Cell (Shape Layout Section)

Legt fest, wie ein platzierbares Shape auf dem Zeichenblatt gekippt und/oder gedreht wird, wenn Sie Shapes unter Verwendung des Dialogfelds **Layout konfigurieren** ausrichten. (Klicken Sie dazu auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu anordnen**, und klicken Sie dann auf **Weitere Layoutoptionen**.)
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
|0  <br/> |Zeichenblattstandard verwenden:  <br/> |**visLOFlipDefault** <br/> |
|1  <br/> |Horizontal kippen.  <br/> |**visLOFlipX** <br/> |
|2  <br/> |Vertikal kippen.  <br/> |**visLOFlipY** <br/> |
|4  <br/> |In 90-Grad-Schritten zwischen 0 und 270 kippen.  <br/> |**visLOFlipRotate** <br/> |
|8  <br/> |Nicht kippen.  <br/> |**visLOFlipNone** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Der Wert in der Zelle ShapePlaceFlip hilft bei der Ausrichtung eines platzierbaren Shapes in Richtung des nächsten platzierbaren Shapes, mit dem es verbunden ist.
  
Wenn Sie dieses Verhalten für *sämtliche* Shapes auf dem Zeichenblatt festlegen möchten, verwenden Sie die Zelle PlaceFlip im Abschnitt Page Layout. 
  
Wenn Sie einen Verweis auf die Zelle ShapePlaceFlip aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |ShapePlaceFlip  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ShapePlaceFlip aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
|Zellenindex:  <br/> |**visSLOPlaceFlip** <br/> |
   

