---
title: Zelle "TxtLocPinX" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
ms.localizationpriority: medium
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Bestimmt die X-Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 019ebd40029c2c07c534a65e81f74bfaca91ac7a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559395"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>Zelle "TxtLocPinX" (Abschnitt "Text Transform")

Bestimmt die  X-Koordinate des Drehmittelpunkts des Textblocks im Verhältnis zum Ursprung des Textblocks. Die Standardformel lautet: 
  
= TxtWidth \* 0,5
  
Diese Formel berechnet die horizontale Mitte des Textblocks.
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle TxtLocPinX anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtLocPinX  <br/> |
   
Um einen Verweis auf die Zelle TxtLocPinX anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinX** <br/> |
   

