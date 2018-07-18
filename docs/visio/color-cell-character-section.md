---
title: Zelle "Color" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Bestimmt die für den Text des Shapes verwendete Farbe.
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796630"
---
# <a name="color-cell-character-section"></a>Color Cell (Character Section)

Bestimmt die für den Text des Shapes verwendete Farbe.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Um eine benutzerdefinierte Farbe eingeben möchten, verwenden Sie die RGB oder HSL-Funktion. Der Wert einer benutzerdefinierten Farbe ist ihre RGB-Farbe und RGB ( *R, g, b*), anstatt eine Zahl in das ShapeSheet-Fenster angezeigt werden. Bei Verwendung in numerischen Operationen haben benutzerdefinierte Farben Werte von 24 und höher. 
  
Die Transparenz der Textfarbe können Sie in der Zelle Transparenz festlegen.
  
Wenn Sie einen Verweis auf die Zelle Color aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.Color [ *i* ] wobei *i* = < 1 >, 2, 3,...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Color aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2,...  <br/> |
|Zellenindex:  <br/> |**visCharacterColor** <br/> |
   

