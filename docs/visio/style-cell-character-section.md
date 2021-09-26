---
title: Zelle "Style" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
ms.localizationpriority: medium
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Zeigt die Zeichenformatierung für einen Textbereich im Textblock des Shapes an.
ms.openlocfilehash: 4171ceac4ea092b3ed70bb06c11b1113d61ef1b5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603389"
---
# <a name="style-cell-character-section"></a>Zelle "Style" (Abschnitt "Character")

Zeigt die Zeichenformatierung für einen Textbereich im Textblock des Shapes an.
  
|**Style**|**Wert**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Fett  <br/> | &amp;H1  <br/> |**visBold** <br/> |
| Kursiv  <br/> | &amp;H2  <br/> |**visItalic** <br/> |
| Unterstrichen  <br/> | &amp;H4  <br/> |**visUnderLine** <br/> |
| Kapitälchen  <br/> | &amp;H8  <br/> |**visSmallCaps** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Zelle Style enthält Formatierungsinformationen für einen Unterbereich des Texts eines Shapes, wenn der Abschnitt Character mehrere Zeilen enthält. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.
  
Der Wert stellt eine Binärzahl dar, in der jedes einzelne Bit eine Zeichenformatvorlage ist. Der Wert 3 stellt beispielsweise fett und kursiv formatierten Text dar. Wenn der Wert von Style 0 ist, ist der Text überhaupt nicht formatiert. Sie können ein bestimmtes Format mit booleschen \* BIT-Funktionen testen. Ausführliche Informationen zu diesen Funktionen finden Sie in Ihrer Programmierungsdokumentation.
  
Um einen Verweis auf die Zelle Style anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Char.Style[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Style anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
| Zeilenindex:  <br/> |**visRowCharacter**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCharacterStyle** <br/> |
   
 *Beispiel* 
  
Die Zelle Farbe in der ersten Zeile des Abschnitts Character eines Shapes enthält die folgende Formel:
  
= IF(BITAND(Char.Style,1)=1,4,3)
  
Wenn das erste Zeichen des Shape-Texts fett formatiert ist, ist der von der ersten Zeile mit Zeicheneigenschaften formatierte Text blau (4). Andernfalls ist er grün (3). Dieses Beispiel setzt voraus, dass die Standardfarben verwendet werden.
  
Nachfolgend finden Sie ein Beispiel zum Festlegen eines Werts für die Zelle Style in einem Programm. Der erste Befehl verweist namentlich auf die Zelle Style, und der zweite Befehl verweist per Index auf die Zelle Style. Mit beiden Befehlen wird der von der zweiten Zeile des Abschnitts Character eines Shapes abgedeckte Text kursiv formatiert.
  

