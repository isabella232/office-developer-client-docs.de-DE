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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405422"
---
# <a name="bulletsize-cell-paragraph-section"></a>Zelle "BulletSize" (Abschnitt "Paragraph")

Gibt die Größe eines Aufzählungszeichens an. 
  
## <a name="remarks"></a>Hinweise

Dieser Wert kann sowohl für vordefinierte als auch für benutzerdefinierte Aufzählungszeichen als Prozentsatz oder als spezifischer Wert angegeben werden. 
  
Wenn der Wert null (0) ist, hat das Aufzählungszeichen dieselbe Schriftgröße wie das erste Zeichen im Absatz. Wenn der Wert ein Prozentsatz ist, erhält das Aufzählungszeichen einen Schriftgrad, der prozentual vom Schriftgrad des ersten Zeichens im Absatz abgeleitet wird. Negative Zahlen werden als Prozentsätze behandelt.
  
Um einen Verweis auf die Zelle BulletSize anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.BulletFontSize[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die BulletSize-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visBulletFontSize** <br/> |
   

