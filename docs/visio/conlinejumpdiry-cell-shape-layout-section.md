---
title: Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404771"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")

Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.
  
|**Wert**|**Liniensprungrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Zeichenblattstandard  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Nach links  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Nach rechts  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie die Zelle  PageLineJumpDirY im Abschnitt Seitenlayout, um die standardmäßige vertikale Richtung für alle Verbindersprünge auf einer Seite zu festlegen. 
  
Um einen Verweis auf die Zelle ConLineJumpDirY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ConLineJumpDirY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die ConLineJumpDirY-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOJumpDirY** <br/> |
   

