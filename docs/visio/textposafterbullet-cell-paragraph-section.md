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
ms.openlocfilehash: fe22b81113ab6537922ad4627aa53f34f2e62c48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798254"
---
# <a name="textposafterbullet-cell-paragraph-section"></a>TextPosAfterBullet Cell (Paragraph Section)

Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar. 
  
## <a name="remarks"></a>Hinweise

Dieser Abstand wird zum Abstand in der Zelle IndFirst addiert, der den Standardeinzug links darstellt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. 
  
Wenn Sie einen Verweis auf die Zelle TextPosAfterBullet nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.TextPosAfterBullet [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TextPosAfterBullet aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visTextPosAfterBullet** <br/> |
   

