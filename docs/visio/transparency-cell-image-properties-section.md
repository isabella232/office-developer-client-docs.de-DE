---
title: Zelle "Transparency" (Abschnitt "Image Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51095
localization_priority: Normal
ms.assetid: 5b265356-1602-4241-fbe1-4d5a55392a52
description: Legt die Transparenzstufe für eine Layerfarbe fest.
ms.openlocfilehash: 5537cbdcd49c66f3bc28a58051f6e2888a290cd3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798299"
---
# <a name="transparency-cell-image-properties-section"></a>Transparency Cell (Image Properties Section)

Legt die Transparenzstufe für eine Layerfarbe fest.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0 – 100  <br/> |Stellt die Transparenz in Prozent dar. Der Standardwert ist 0% (vollständig undurchsichtig).  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Werte werden auf die nächste halbe % gerundet. Es wird ein Wert von 100 % vollständig transparent. Obwohl einem Layer, vollständig transparente Farbe ist, die gleiche auf dem Zeichenblatt als einer Ebene angezeigt, die keine Farbe aufweist wird, die Interaktion mit anderen Objekten auf der Seite auf die gleiche Weise als wäre die Transparenz 0 %. Sie können diesen Wert auch festlegen, mit den Schieberegler im Dialogfeld **Layereigenschaften** (klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** , klicken Sie auf **Ebenen**, und klicken Sie dann auf **Layereigenschaften**).
  
Wenn Sie einen Verweis auf die Zelle Transparency nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Transparency  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Transparency aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowImage** <br/> |
|Zellenindex:  <br/> |**visImageTransparency** <br/> |
   

