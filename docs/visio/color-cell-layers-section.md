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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341825"
---
# <a name="color-cell-layers-section"></a>Zelle "Color" (Abschnitt "Layers")

Gibt die zur Darstellung des Layers verwendete Farbe an.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Dieser Zellenwert entspricht der Einstellung **Layer-Farbe** im Dialog **Feld Layereigenschaften** (Klicken Sie auf der Registerkarte **Start** in der Gruppe **Bearbeiten** auf **** Layer, und klicken Sie dann auf **Layereigenschaften**).
  
Verwenden Sie die RGB-oder die GSL-Funktion, um eine benutzerdefinierte Farbe einzugeben. Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe, und RGB ( *r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt. Bei numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher. Der Wert 255 gibt an, dass die Ebene keine Farbe aufweist. 
  
Die Transparenz der Layer-Farbe können Sie in der Zelle Transparenz festlegen.
  
Wenn Sie einen Verweis auf die Zelle Farbe aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers. Color [ *i* ] wobei *i* = <1>, 2, 3,...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Color nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**visRowLayer** +  *i* , wobei *i* = 0, 1, 2,...  <br/> |
|Zellenindex:  <br/> |**visLayerColor** <br/> |
   

