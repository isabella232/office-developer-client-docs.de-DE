---
title: Zelle "BulletSize" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
localization_priority: Normal
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Gibt die Größe eines Aufzählungszeichens an.
ms.openlocfilehash: 8671bc6f5ec40814b13727bc458f74eb2893f839
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337611"
---
# <a name="bulletsize-cell-paragraph-section"></a>Zelle "BulletSize" (Abschnitt "Paragraph")

Gibt die Größe eines Aufzählungszeichens an. 
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert kann sowohl für vordefinierte als auch für benutzerdefinierte Aufzählungszeichen als Prozentsatz oder als spezifischer Wert angegeben werden. 
  
Wenn der Wert NULL (0) ist, hat das Aufzählungszeichen den gleichen Schriftgrad wie der erste Buchstabe im Absatz. Wenn der Wert ein Prozentsatz ist, erhält das Aufzählungszeichen einen Schriftgrad, der prozentual vom Schriftgrad des ersten Zeichens im Absatz abgeleitet wird. Negative Zahlen werden als Prozentsätze behandelt.
  
Wenn Sie einen Verweis auf die Zelle Zelle BulletSize aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Abs. BulletFontSize [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle BulletSize aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visBulletFontSize** <br/> |
   

