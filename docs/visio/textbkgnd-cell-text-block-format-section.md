---
title: Zelle "TextBkgnd" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: Legt die Farbe des Texthintergrunds für ein Shape fest.
ms.openlocfilehash: 2256a4c89812924af820c020c225f4b82b1d4856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798264"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>TextBkgnd Cell (Text Block Format Section)

Legt die Farbe des Texthintergrunds für ein Shape fest.
  
## <a name="remarks"></a>Bemerkungen

Die Zelle TextBkgnd kann einen beliebigen Wert von 0 bis 24 oder 255 haben. Die Werte 0 und 255 ( *VisTxtBlklOpaque*) Geben Sie einen transparenten Texthintergrund an. 
  
Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die Funktionen RGB oder HSL plus 1 – beispielsweise RGB (255,127,255) + 1. Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*) + 1, statt eine Zahl in das ShapeSheet-Fenster angezeigt werden. Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 25 und höher. 
  
Die Transparenz der Texthintergrundfarbe können Sie in der Zelle TextBkgnd Trans festlegen.
  
Zum Abrufen eines Verweises auf die Zelle TextBkgnd nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |TextBkgnd  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TextBkgnd aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowText** <br/> |
|Zellenindex:  <br/> |**visTxtBlkBkgnd** <br/> |
   

