---
title: Zelle "TxtLocPinY" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
ms.localizationpriority: medium
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Bestimmt die y-Koordinate des Drehmittelpunkts des Textblocks relativ zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 745a067a6ac7aca50e2bd2789fb9951bc96e2595
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627247"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>Zelle "TxtLocPinY" (Abschnitt "Text Transform")

Bestimmt die  y-Koordinate des Drehmittelpunkts des Textblocks relativ zum Ursprung des Textblocks. Die Standardformel lautet: 
  
= TxtHeight \* 0,5
  
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle TxtLocPinY anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtLocPinY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TxtLocPinY anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinY** <br/> |
   

