---
title: Zelle "IndRight" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
ms.localizationpriority: medium
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom rechten Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der rechte Einzug gleich.
ms.openlocfilehash: 7689d808f8c1cc886a20488251ae75418c1d8af8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570456"
---
# <a name="indright-cell-paragraph-section"></a>Zelle "IndRight" (Abschnitt "Paragraph")

Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom rechten Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der rechte Einzug gleich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle "IndRight" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.IndRight[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle "IndRight" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visIndentRight** <br/> |
   

