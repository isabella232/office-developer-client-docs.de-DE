---
title: Zelle "Color" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Gibt die zur Darstellung des Layers verwendete Farbe an.
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435131"
---
# <a name="color-cell-layers-section"></a>Zelle "Color" (Abschnitt "Layers")

Gibt die zur Darstellung des Layers verwendete Farbe an.
  
## <a name="remarks"></a>Hinweise

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Dieser Zellwert entspricht der  Einstellung **Layer-Farbe** im Dialogfeld  **Layereigenschaften** (klicken Sie in der Gruppe Bearbeiten auf der Registerkarte **Start** auf Ebenen und dann auf **Layereigenschaften**).
  
Verwenden Sie zum Eingeben einer benutzerdefinierten Farbe die RGB- oder HSL-Funktion. Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*), anstatt eine Zahl, wird im ShapeSheet-Fenster angezeigt. Bei Verwendung in numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher. Der Wert 255 gibt an, dass die Ebene keine Farbe hat. 
  
Die Transparenz der Layer-Farbe können Sie in der Zelle Transparenz festlegen.
  
Um einen Verweis auf die Zelle Color anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Color[ *i*  ] where  *i*  = <1>, 2, 3, ...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Color nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer**  +   *i* where *i* = 0, 1, 2, ...  <br/> |
|Zellenindex:  <br/> |**visLayerColor** <br/> |
   

