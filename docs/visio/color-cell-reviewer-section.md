---
title: Zelle "Color" (Abschnitt "Reviewer")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
ms.localizationpriority: medium
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Ein RGB-Wert, der die Farbe darstellt, die dem Markup eines Dokumentprüfers zugewiesen ist.
ms.openlocfilehash: a5b34ad4902a7b6ba2e8143c358533fb235467b6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566073"
---
# <a name="color-cell-reviewer-section"></a>Zelle "Color" (Abschnitt "Reviewer")

Ein RGB-Wert, der die Farbe darstellt, die dem Markup eines Dokumentprüfers zugewiesen ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Farben werden Bearbeitern in der folgenden Reihenfolge zugewiesen: Rot, Blau, Grün, Violett, Orange, Türkis, Grau. Diese Farben werden für alle verbleibenden Bearbeiter erneut durchlaufen. 
  
Kommentare auf dem ursprünglichen Zeichenblatt weisen stets die Farbe Gelb auf, ungeachtet der Farbe, die einem Bearbeiter in der Zelle Color zugewiesen ist. 
  
Um einen Verweis auf die Zelle "Color" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Reviewer.Color [  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Color anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionReviewer** <br/> |
| Zeilenindex:  <br/> |**visRowReviewer**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visReviewerColor** <br/> |
   

