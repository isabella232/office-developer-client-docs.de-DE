---
title: Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
ms.localizationpriority: medium
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: 1e5d19f4f8268b02439889d4448c0ca844850c4e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594741"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")

Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.
  
|**Wert**|**Liniensprungrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Zeichenblattstandard  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Nach links  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Nach rechts  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um die vertikale Standardrichtung für  *alle*  Verbindersprünge auf einer Seite festzulegen, verwenden Sie die Zelle "PageLineJumpDirY" im Abschnitt "Seitenlayout". 
  
Um einen Verweis auf die Zelle "ConLineJumpDirY" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ConLineJumpDirY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ConLineJumpDirY anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOJumpDirY** <br/> |
   

