---
title: Zelle "Color" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
ms.localizationpriority: medium
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: Bestimmt die für den Text des Shapes verwendete Farbe.
ms.openlocfilehash: bff5857a8351004304e75b6000e2937372f9e905
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608487"
---
# <a name="color-cell-character-section"></a>Zelle "Color" (Abschnitt "Character")

Bestimmt die für den Text des Shapes verwendete Farbe.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie die Farbe festlegen möchten, geben Sie eine Zahl von 0 bis 23 ein.
  
Verwenden Sie die RGB- oder HSL-Funktion, um eine benutzerdefinierte Farbe einzugeben. Der Wert einer benutzerdefinierten Farbe ist die RGB-Farbe, und RGB( *r, g, b*) anstelle einer Zahl wird im ShapeSheet-Fenster angezeigt. Bei verwendung in numerischen Vorgängen weisen benutzerdefinierte Farben Werte von 24 und höher auf. 
  
Die Transparenz der Textfarbe können Sie in der Zelle Transparenz festlegen.
  
Um einen Verweis auf die Zelle "Color" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char.Color[ *i*  ] where  *i*  = <1>, 2, 3, ...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Color anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter**  +   *i* where *i* = 0, 1, 2, ...  <br/> |
|Zellenindex:  <br/> |**visCharacterColor** <br/> |
   

