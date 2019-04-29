---
title: Zelle "BulletFont" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
localization_priority: Normal
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Stellt die Nummer der Schriftart dar, die zum Formatieren von Text verwendet wird, wenn eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge angegeben ist und der Wert in der Zelle Bullet ungleich Null ist.
ms.openlocfilehash: 1cf04917bb7dfa68ee9395abb66ffe9e150f0273
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438463"
---
# <a name="bulletfont-cell-paragraph-section"></a>Zelle "BulletFont" (Abschnitt "Paragraph")

Stellt die Nummer der Schriftart dar, die zum Formatieren von Text verwendet wird, wenn eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge angegeben ist und der Wert in der Zelle Bullet ungleich Null ist. 
  
## <a name="remarks"></a>Bemerkungen

Nummern von Schriftarten variieren entsprechend der im System installierten Schriftarten. Wenn der Wert 0 und eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge vorhanden ist, entspricht die verwendete Schriftart der Schriftart des ersten Zeichens des Absatzes.
  
Wenn Sie einen Verweis auf die Zelle Zelle BulletFont aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Abs. Zelle BulletFont [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle BulletFont aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visBulletFont** <br/> |
   

