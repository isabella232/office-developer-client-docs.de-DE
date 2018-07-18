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
ms.openlocfilehash: b6728d44c71f6403e772a6a7e730ba3c18d9eb48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796647"
---
# <a name="color-cell-layers-section"></a>Color Cell (Layers Section)

Gibt die zur Darstellung des Layers verwendete Farbe an.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Dieser Zellwert entspricht der Einstellung für **Layerfarbe** im Dialogfeld **Layereigenschaften** (in der Gruppe **Bearbeiten** auf der Registerkarte **Start** , klicken Sie auf **Ebenen** und klicken Sie dann auf **Layereigenschaften**).
  
Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB oder HSL-Funktion. Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*), anstatt eine Zahl in das ShapeSheet-Fenster angezeigt werden. Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 24 und höher. Der Wert 255 gibt an, dass der Layer keine Farbe aufweist. 
  
Die Transparenz der Layer-Farbe können Sie in der Zelle Transparenz festlegen.
  
Wenn Sie einen Verweis auf die Zelle Color aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Layers.Color [ *i* ] wobei *i* = < 1 >, 2, 3,...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Color aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionLayer** <br/> |
|Zeilenindex:  <br/> |**VisRowLayer** +  *i* wobei *i* = 0, 1, 2,...  <br/> |
|Zellenindex:  <br/> |**visLayerColor** <br/> |
   

