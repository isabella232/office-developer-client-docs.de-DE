---
title: Zelle "TxtHeight" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
ms.localizationpriority: medium
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Definiert die Höhe eines Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: bcf9292de38860ebfbb81607049214cd5ce99aa7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553675"
---
# <a name="txtheight-cell-text-transform-section"></a>Zelle "TxtHeight" (Abschnitt "Text Transform")

Definiert die Höhe eines Textblocks. Die Standardformel lautet:
  
= Höhe \* 1
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle TxtHeight anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtHeight  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TxtHeight anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormHeight** <br/> |
   

