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
description: Ein RGB-Wert, der die Farbe darstellt, die dem Markup eines Dokument Bearbeiters zugewiesen ist.
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430539"
---
# <a name="color-cell-reviewer-section"></a>Zelle "Color" (Abschnitt "Reviewer")

Ein RGB-Wert, der die Farbe darstellt, die dem Markup eines Dokument Bearbeiters zugewiesen ist. 
  
## <a name="remarks"></a>Bemerkungen

Farben werden Bearbeitern in der folgenden Reihenfolge zugewiesen: Rot, Blau, Grün, Violett, Orange, Türkis, Grau. Diese Farben werden für alle verbleibenden Bearbeiter erneut durchlaufen. 
  
Kommentare auf dem ursprünglichen Zeichenblatt weisen stets die Farbe Gelb auf, ungeachtet der Farbe, die einem Bearbeiter in der Zelle Color zugewiesen ist. 
  
Wenn Sie einen Verweis auf die Zelle Farbe aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Prüfer. Color [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Color nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionReviewer** <br/> |
| Zeilenindex:  <br/> |**visRowReviewer** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visReviewerColor** <br/> |
   

