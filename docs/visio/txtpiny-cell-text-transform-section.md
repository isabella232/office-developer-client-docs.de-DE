---
title: Zelle "TxtPinY" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
ms.localizationpriority: medium
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Bestimmt die y-Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet:'
ms.openlocfilehash: a08e1da3a7e36cf7bfd04d199a949dfe91d6df33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603235"
---
# <a name="txtpiny-cell-text-transform-section"></a>Zelle "TxtPinY" (Abschnitt "Text Transform")

Bestimmt die  y-Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet: 
  
= Höhe \* 0,5
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle TxtPinY anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtPinY  <br/> |
   
Um einen Verweis auf die Zelle TxtPinY anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormPinY** <br/> |
   

