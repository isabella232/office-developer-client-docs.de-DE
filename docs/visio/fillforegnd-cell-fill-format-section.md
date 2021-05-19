---
title: Zelle "FillForegnd" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: Legt die Farbe fest, die für den Vordergrund (Pinselstrich) des Füllmusters des Shapes verwendet wird.
ms.openlocfilehash: 352fecf8d99069cfb5ebd72d295284dc03446364
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415565"
---
# <a name="fillforegnd-cell-fill-format-section"></a>Zelle "FillForegnd" (Abschnitt "Fill Format")

Legt die Farbe fest, die für den Vordergrund (Pinselstrich) des Füllmusters des Shapes verwendet wird.
  
## <a name="remarks"></a>Hinweise

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Verwenden Sie zum Eingeben einer benutzerdefinierten Farbe die RGB- oder HSL-Funktion. Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*), anstatt eine Zahl, wird im ShapeSheet-Fenster angezeigt. Bei Verwendung in numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher. 
  
Die Fülltransparenz für den Vordergrund können Sie in der Zelle FüllbereichVGrundTrans festlegen.
  
Um einen Verweis auf die FillForegnd-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |FillForegnd  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die FillForegnd-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowFill** <br/> |
|Zellenindex:  <br/> |**visFillForegnd** <br/> |
   

