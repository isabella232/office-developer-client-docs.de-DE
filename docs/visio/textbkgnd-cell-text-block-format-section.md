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
ms.openlocfilehash: 2450bf0cb0e013c0f9310eacfca0f5a20e7e6063
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406542"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>Zelle "TextBkgnd" (Abschnitt "Text Block Format")

Legt die Farbe des Texthintergrunds für ein Shape fest.
  
## <a name="remarks"></a>Bemerkungen

Die Zelle TextBkgnd-Zelle kann einen beliebigen Wert von 0 bis 24 oder 255 haben. Die Werte 0 und 255 ( *visTxtBlklOpaque*) deuten auf einen transparenten Texthintergrund hin. 
  
Wenn Sie eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB-oder die GSL-Funktion plus eine, beispielsweise RGB (255127255) + 1. Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB ( *r, g, b*) + 1 anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt. Bei numerischen Vorgängen haben benutzerdefinierte Farben Werte von 25 und höher. 
  
Die Transparenz der Texthintergrundfarbe können Sie in der Zelle TextBkgnd Trans festlegen.
  
Wenn Sie einen Verweis auf die Zelle Zelle TextBkgnd aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Zelle TextBkgnd  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle TextBkgnd aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowText** <br/> |
|Zellenindex:  <br/> |**visTxtBlkBkgnd** <br/> |
   

