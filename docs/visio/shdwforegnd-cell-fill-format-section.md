---
title: Zelle "ShdwForegnd" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251244
localization_priority: Normal
ms.assetid: ea153390-631d-79fd-c1ba-4c281239a24e
description: Legt die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.
ms.openlocfilehash: 602df83dcb88d4137b0609f9a8b1084a40148a10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422250"
---
# <a name="shdwforegnd-cell-fill-format-section"></a>Zelle "ShdwForegnd" (Abschnitt "Fill Format")

Legt die Farbe fest, die für den Vordergrund (Pinselstrich) des Schattenfüllmusters des Shapes verwendet wird.
  
## <a name="remarks"></a>Hinweise

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Verwenden Sie zum Eingeben einer benutzerdefinierten Farbe die RGB- oder HSL-Funktion. Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*), anstatt eine Zahl, wird im ShapeSheet-Fenster angezeigt. Bei Verwendung in numerischen Vorgängen haben benutzerdefinierte Farben Werte von 24 und höher. 
  
Sie können die Transparenz der Farbe für den Vordergrund des Schattenfüllmusters des Shapes in der Zelle ShdwForegndTrans festlegen.
  
Um einen Verweis auf die Zelle ShdwForegnd anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShdwForegnd  <br/> |
   
Um einen Verweis auf die ShdwForegnd-Zelle nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowFill** <br/> |
| Zellenindex:  <br/> |**visFillShdwForegnd** <br/> |
   

