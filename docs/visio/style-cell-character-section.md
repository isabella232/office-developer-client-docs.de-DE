---
title: Zelle "Style" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251249
localization_priority: Normal
ms.assetid: 4372f1e1-f0a9-2f63-ff79-58f2afdceed5
description: Zeigt die Zeichenformatierung für einen Textbereich im Textblock des Shapes an.
ms.openlocfilehash: 48bda5eb798f439e2616b2b910d7ec5ac719d060
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798192"
---
# <a name="style-cell-character-section"></a>Style Cell (Character Section)

Zeigt die Zeichenformatierung für einen Textbereich im Textblock des Shapes an.
  
|**Style**|**Wert**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| Fett  <br/> | &amp;H1  <br/> |**visBold** <br/> |
| Kursiv  <br/> | &amp;H2  <br/> |**visItalic** <br/> |
| Unterstrichen  <br/> | &amp;H4  <br/> |**visUnderLine** <br/> |
| Kapitälchen  <br/> | &amp;H8  <br/> |**visSmallCaps** <br/> |
   
## <a name="remarks"></a>Hinweise

Die Zelle Style enthält Formatierungsinformationen für einen Unterbereich des Texts eines Shapes, wenn der Abschnitt Character mehrere Zeilen enthält. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.
  
Der Wert stellt eine binäre Zahl in denen jedes Bit eine Zeichenformatvorlage angibt. Beispielsweise stellt einen Wert von 3 Text fett und kursiv formatiert. Wenn der Wert der Style 0 ist, wird der Text einfache oder unformatierte. Sie können ein bestimmtes Format mit Boolean BIT testen\* Funktionen. Finden Sie unter Dokumentation zu Ihrem Programmierung Informationen zu diesen Funktionen.
  
Wenn Sie einen Verweis auf die Zelle Style aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Char.Style [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Style aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
| Zeilenindex:  <br/> |**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCharacterStyle** <br/> |
   
 *Beispiel* 
  
Die Zelle Farbe in der ersten Zeile des Abschnitts Character eines Shapes enthält die folgende Formel:
  
= IF(BITAND(Char.Style,1)=1,4,3)
  
Wenn das erste Zeichen des Shape-Texts fett formatiert ist, ist der von der ersten Zeile mit Zeicheneigenschaften formatierte Text blau (4). Andernfalls ist er grün (3). Dieses Beispiel setzt voraus, dass die Standardfarben verwendet werden.
  
Nachfolgend finden Sie ein Beispiel zum Festlegen eines Werts für die Zelle Style in einem Programm. Der erste Befehl verweist namentlich auf die Zelle Style, und der zweite Befehl verweist per Index auf die Zelle Style. Mit beiden Befehlen wird der von der zweiten Zeile des Abschnitts Character eines Shapes abgedeckte Text kursiv formatiert.
  

