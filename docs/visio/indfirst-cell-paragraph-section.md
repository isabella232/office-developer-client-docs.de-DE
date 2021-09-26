---
title: Zelle "IndFirst" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
ms.localizationpriority: medium
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Stellt den Abstand dar, den die erste Zeile jedes einzelnen Absatzes im Textblock des Shapes vom linken Einzug des Absatzes eingezogen ist. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der Einzug der ersten Zeile gleich.
ms.openlocfilehash: 16b3d13afa81958d1b428b417c28683441703fd9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612603"
---
# <a name="indfirst-cell-paragraph-section"></a>Zelle "IndFirst" (Abschnitt "Paragraph")

Stellt den Abstand dar, den die erste Zeile jedes einzelnen Absatzes im Textblock des Shapes vom linken Einzug des Absatzes eingezogen ist. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der Einzug der ersten Zeile gleich.
  
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle "IndFirst" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.IndFirst[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle "IndFirst" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visIndentFirst** <br/> |
   

