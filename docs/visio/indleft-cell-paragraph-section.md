---
title: Zelle "IndLeft" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251255
localization_priority: Normal
ms.assetid: 31a7d0d4-4666-ddef-c5eb-4d13803e6a2f
description: Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom linken Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der linke Einzug gleich.
ms.openlocfilehash: 2a942ef3d874b8d1ce2ef85f423c93bc0db33230
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405163"
---
# <a name="indleft-cell-paragraph-section"></a>Zelle "IndLeft" (Abschnitt "Paragraph")

Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom linken Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der linke Einzug gleich.
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle IndLeft anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.IndLeft[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die IndLeft-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visIndentLeft** <br/> |
   

