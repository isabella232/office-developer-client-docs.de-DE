---
title: Zelle "BulletSize" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033780
ms.localizationpriority: medium
ms.assetid: 6ff5d07b-17e2-f6ca-1860-5d498a9ebf06
description: Gibt die Größe eines Aufzählungszeichens an.
ms.openlocfilehash: 97f22bc3e4071757de1336dca2efd2b4f1e12c41
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623544"
---
# <a name="bulletsize-cell-paragraph-section"></a>Zelle "BulletSize" (Abschnitt "Paragraph")

Gibt die Größe eines Aufzählungszeichens an. 
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert kann sowohl für vordefinierte als auch für benutzerdefinierte Aufzählungszeichen als Prozentsatz oder als spezifischer Wert angegeben werden. 
  
Wenn der Wert Null (0) ist, hat das Aufzählungszeichen denselben Schriftgrad wie das erste Zeichen im Absatz. Wenn der Wert ein Prozentsatz ist, erhält das Aufzählungszeichen einen Schriftgrad, der prozentual vom Schriftgrad des ersten Zeichens im Absatz abgeleitet wird. Negative Zahlen werden als Prozentsätze behandelt.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "BulletSize" anhand des Namens aus einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.BulletFontSize[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "BulletSize" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visBulletFontSize** <br/> |
   

