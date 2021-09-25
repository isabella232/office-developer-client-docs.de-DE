---
title: Zelle "HAlign" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
ms.localizationpriority: medium
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Definiert die horizontale Ausrichtung des Texts im Textblock des Shapes.
ms.openlocfilehash: 39f53eeeaed0225f7140f0ab164017d9dada7744
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570620"
---
# <a name="halign-cell-paragraph-section"></a>Zelle "HAlign" (Abschnitt "Paragraph")

Definiert die horizontale Ausrichtung des Texts im Textblock des Shapes.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Linksbündig  <br/> |**visHorzLeft** <br/> |
| 1  <br/> | Zentriert  <br/> |**visHorzCenter** <br/> |
| 2  <br/> | Rechtsbündig  <br/> |**visHorzRight** <br/> |
| 3  <br/> | Ausrichten  <br/> |**visHorzJustify** <br/> |
| 4   <br/> | Blocksatz erzwingen  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Beim Blocksatz wird Platz zwischen den Wörtern in jeder Zeile (nicht in der letzten Zeile) des Absatzes geschaffen, um sowohl die rechte als auch die linke Seite von Text an den Seitenrändern auszurichten.
  
Bei Blocksatz erzwingen wird jede Zeile im Absatz ausgerichtet, einschließlich der letzten Zeile.
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "HAlign" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.HorzAlign[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle "HAlign" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHorzAlign** <br/> |
   

