---
title: Zelle "TxtLocPinY" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Bestimmt die y-Koordinate der Drehmitte des Textblocks relativ zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414060"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>Zelle "TxtLocPinY" (Abschnitt "Text Transform")

Bestimmt  die y-Koordinate der Drehmitte des Textblocks relativ zum Ursprung des Textblocks. Die Standardformel lautet: 
  
= TxtHeight \* 0,5
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle TxtLocPinY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtLocPinY  <br/> |
   
Um einen Verweis auf die Zelle TxtLocPinY nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinY** <br/> |
   

