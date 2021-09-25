---
title: Zelle "TextBkgnd" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
ms.localizationpriority: medium
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Legt die Farbe des Texthintergrunds für ein Shape fest.
ms.openlocfilehash: f8c564a3caf6685ffe0cb0babd3c06cb9a89b11e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559409"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>Zelle "TextBkgnd" (Abschnitt "Text Block Format")

Legt die Farbe des Texthintergrunds für ein Shape fest.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Zelle TextBkgnd kann einen beliebigen Wert zwischen 0 und 24 oder 255 aufweisen. Die Werte 0 und 255 ( *visTxtBlklOpaque*) geben beide einen transparenten Texthintergrund an. 
  
Verwenden Sie zum Eingeben einer benutzerdefinierten Farbe die RGB- oder HSL-Funktion plus eine, z. B. RGB(255,127,255)+1. Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*)+1 anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt. Bei verwendung in numerischen Vorgängen weisen benutzerdefinierte Farben Werte von 25 und höher auf. 
  
Die Transparenz der Texthintergrundfarbe können Sie in der Zelle TextBkgnd Trans festlegen.
  
Um einen Verweis auf die Zelle "TextBkgnd" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |TextBkgnd  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TextBkgnd anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowText** <br/> |
|Zellenindex:  <br/> |**visTxtBlkBkgnd** <br/> |
   

