---
title: Zelle "Color" (Abschnitt "Layers")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
ms.localizationpriority: medium
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: Gibt die zur Darstellung des Layers verwendete Farbe an.
ms.openlocfilehash: bc0f08fbac4a542221e47f0f85b36ba15d2c1159
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577976"
---
# <a name="color-cell-layers-section"></a>Zelle "Color" (Abschnitt "Layers")

Gibt die zur Darstellung des Layers verwendete Farbe an.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Dieser Zellwert entspricht der **Layer-Farbeinstellung** im Dialogfeld **Layereigenschaften** (klicken Sie in der Gruppe **"Bearbeiten"** auf der Registerkarte **"Start"** auf **"Layer",** und klicken Sie dann auf **"Layereigenschaften").**
  
Verwenden Sie die RGB- oder HSL-Funktion, um eine benutzerdefinierte Farbe einzugeben. Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt. Bei verwendung in numerischen Vorgängen weisen benutzerdefinierte Farben Werte von 24 und höher auf. Der Wert 255 gibt an, dass die Ebene keine Farbe hat. 
  
Die Transparenz der Layer-Farbe können Sie in der Zelle Transparenz festlegen.
  
Um einen Verweis auf die Zelle "Color" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Color[ *i*  ] where  *i*  = <1>, 2, 3, ...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Color anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer**  +   *i* where *i* = 0, 1, 2, ...  <br/> |
|Zellenindex:  <br/> |**visLayerColor** <br/> |
   

