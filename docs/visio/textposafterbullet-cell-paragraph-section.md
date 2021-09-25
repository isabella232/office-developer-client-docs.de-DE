---
title: Zelle "TextPosAfterBullet" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
ms.localizationpriority: medium
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar.
ms.openlocfilehash: 7568babf9d23c1055ce4a68955b43cb98c02f94b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559402"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>Zelle "TextPosAfterBullet" (Abschnitt "Paragraph")

Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieser Abstand wird zum Abstand in der Zelle IndFirst addiert, der den Standardeinzug links darstellt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. 
  
Um einen Verweis auf die Zelle "TextPosAfterBullet" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.TextPosAfterBullet[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "TextPosAfterBullet" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visTextPosAfterBullet** <br/> |
   

