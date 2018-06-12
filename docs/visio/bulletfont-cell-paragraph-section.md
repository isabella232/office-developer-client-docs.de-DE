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
ms.openlocfilehash: 7cd3333afc30d30ea7b0e5d35650681074744235
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796573"
---
# <a name="bulletfont-cell-paragraph-section"></a>BulletFont Cell (Paragraph Section)

Stellt die Nummer der Schriftart dar, die zum Formatieren von Text verwendet wird, wenn eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge angegeben ist und der Wert in der Zelle Bullet ungleich Null ist. 
  
## <a name="remarks"></a>Hinweise

Nummern von Schriftarten variieren entsprechend der im System installierten Schriftarten. Wenn der Wert 0 und eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge vorhanden ist, entspricht die verwendete Schriftart der Schriftart des ersten Zeichens des Absatzes.
  
Wenn Sie einen Verweis auf die Zelle BulletFont nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.BulletFont [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle BulletFont aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visBulletFont** <br/> |
   

