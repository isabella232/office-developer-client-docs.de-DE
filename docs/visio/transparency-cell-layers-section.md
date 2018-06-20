---
title: Zelle "Transparency" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Legt die Transparenzstufe für eine Layerfarbe fest.
ms.openlocfilehash: 7c205612436e7731f268e17c851616beebf809dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798305"
---
# <a name="transparency-cell-layers-section"></a>Transparency Cell (Layers Section)

Legt die Transparenzstufe für eine Layerfarbe fest.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 – 100  <br/> |Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte werden auf die nächste halbe % gerundet. Es wird ein Wert von 100 % vollständig transparent. Obwohl einem Layer, vollständig transparente Farbe ist, die gleiche auf dem Zeichenblatt als einer Ebene angezeigt, die keine Farbe aufweist wird, die Interaktion mit anderen Objekten auf der Seite auf die gleiche Weise als wäre die Transparenz 0 %. Sie können diesen Wert auch festlegen, mit den Schieberegler im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** , klicken Sie auf **Ebenen**, und klicken Sie dann auf **Layereigenschaften**).
  
Zum Abrufen eines Verweises auf die Zelle Transparency nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.ColorTrans [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Transparency aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**VisRowLayer** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visLayerColorTrans** <br/> |
   

