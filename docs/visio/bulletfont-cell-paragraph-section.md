---
title: Zelle "BulletFont" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60023
ms.localizationpriority: medium
ms.assetid: a75ff1f3-2f4d-89e3-108b-e16a34f5184f
description: Stellt die Nummer der Schriftart dar, die zum Formatieren von Text verwendet wird, wenn eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge angegeben ist und der Wert in der Zelle Bullet ungleich Null ist.
ms.openlocfilehash: 32c7240ac9cf44c7e37ba5fee003f0b5bc876bd0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603802"
---
# <a name="bulletfont-cell-paragraph-section"></a>Zelle "BulletFont" (Abschnitt "Paragraph")

Stellt die Nummer der Schriftart dar, die zum Formatieren von Text verwendet wird, wenn eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge angegeben ist und der Wert in der Zelle Bullet ungleich Null ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Nummern von Schriftarten variieren entsprechend der im System installierten Schriftarten. Wenn der Wert 0 und eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge vorhanden ist, entspricht die verwendete Schriftart der Schriftart des ersten Zeichens des Absatzes.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "BulletFont" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.BulletFont[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "BulletFont" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visBulletFont** <br/> |
   

