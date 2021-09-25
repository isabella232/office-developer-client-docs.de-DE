---
title: Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm185
ms.localizationpriority: medium
ms.assetid: f0671835-8d48-907a-eca6-43953658f800
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: 2749d1fde3ebcfa6cd5a1c367ea9ce8674925be5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608396"
---
# <a name="conlinejumpdirx-cell-shape-layout-section"></a>Zelle "ConLineJumpDirX" (Abschnitt "Shape Layout")

Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem horizontalen dynamischen Verbinder für ein Shape auftreten.
  
|**Wert**|**Liniensprungrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Zeichenblattstandard  <br/> |**visLOJumpDirXDefault** <br/> |
| 1  <br/> | Nach oben  <br/> |**visLOJumpDirXUp** <br/> |
| 2  <br/> | Nach unten  <br/> |**visLOJumpDirXDown** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um die horizontale Standardrichtung für  *alle*  Verbindersprünge auf einer Seite festzulegen, verwenden Sie die Zelle "PageLineJumpDirX" im Abschnitt "Seitenlayout". 
  
Um einen Verweis auf die Zelle "ConLineJumpDirX" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ConLineJumpDirX  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle "ConLineJumpDirX" anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOJumpDirX** <br/> |
   

