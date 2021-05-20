---
title: Zelle "Color" (Abschnitt "Reviewer")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: Ein RGB-Wert, der die Farbe darstellt, die dem Markup eines Dokumentbeprüfers zugewiesen ist.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430539"
---
# <a name="color-cell-reviewer-section"></a>Zelle "Color" (Abschnitt "Reviewer")

Ein RGB-Wert, der die Farbe darstellt, die dem Markup eines Dokumentbeprüfers zugewiesen ist. 
  
## <a name="remarks"></a>Hinweise

Farben werden Bearbeitern in der folgenden Reihenfolge zugewiesen: Rot, Blau, Grün, Violett, Orange, Türkis, Grau. Diese Farben werden für alle verbleibenden Bearbeiter erneut durchlaufen. 
  
Kommentare auf dem ursprünglichen Zeichenblatt weisen stets die Farbe Gelb auf, ungeachtet der Farbe, die einem Bearbeiter in der Zelle Color zugewiesen ist. 
  
Um einen Verweis auf die Zelle Color anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Reviewer.Color [  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Color nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionReviewer** <br/> |
| Zeilenindex:  <br/> |**visRowReviewer**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visReviewerColor** <br/> |
   

