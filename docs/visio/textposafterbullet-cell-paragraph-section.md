---
title: Zelle "TextPosAfterBullet" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar.
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422152"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>Zelle "TextPosAfterBullet" (Abschnitt "Paragraph")

Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar. 
  
## <a name="remarks"></a>Hinweise

Dieser Abstand wird zum Abstand in der Zelle IndFirst addiert, der den Standardeinzug links darstellt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. 
  
Verwenden Sie folgendes, um einen Verweis auf die Zelle TextPosAfterBullet anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.TextPosAfterBullet[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die TextPosAfterBullet-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visTextPosAfterBullet** <br/> |
   

