---
title: Zelle "TxtPinX" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
ms.localizationpriority: medium
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Bestimmt die X-Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet:'
ms.openlocfilehash: 7cd62258558fc9657a62b1e3e39811acac973527
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59569853"
---
# <a name="txtpinx-cell-text-transform-section"></a>Zelle "TxtPinX" (Abschnitt "Text Transform")

Bestimmt die  X-Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet: 
  
= Breite \* 0,5
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle TxtPinX anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtPinX  <br/> |
   
Um einen Verweis auf die Zelle TxtPinX anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormPinX** <br/> |
   

