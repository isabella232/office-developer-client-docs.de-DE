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
ms.openlocfilehash: e1b6bd1b4535a70bf99b9cd90af3e0d52128da01
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796545"
---
# <a name="bulletsize-cell-paragraph-section"></a>BulletSize Cell (Paragraph Section)

Gibt die Größe eines Aufzählungszeichens an. 
  
## <a name="remarks"></a>Hinweise

Dieser Wert kann sowohl für vordefinierte als auch für benutzerdefinierte Aufzählungszeichen als Prozentsatz oder als spezifischer Wert angegeben werden. 
  
Wenn der Wert NULL (0) ist, wird das Aufzählungszeichen die gleiche Schriftgröße wie das erste Zeichen im Absatz. Wenn der Wert ein Prozentsatz ist, wird das Aufzählungszeichen als Prozentsatz der Schriftgrad des ersten Zeichens im Absatz angepasst. Negative Zahlen werden als Prozentsätze behandelt.
  
Wenn Sie einen Verweis auf die Zelle BulletSize aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.BulletFontSize [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle BulletSize aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visBulletFontSize** <br/> |
   

