---
title: Zelle "TxtPinY" (Abschnitt "Text Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 'Bestimmt die y-Koordinate der Drehmitte des Textblocks im Verhältnis zum Ursprung der Form. Die Standardformel lautet:'
ms.openlocfilehash: fc62ac76aa24a698d956690df6e5d1e7cff3fb5f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418491"
---
# <a name="txtpiny-cell-text-transform-section"></a>Zelle "TxtPinY" (Abschnitt "Text Transform")

Bestimmt  die y-Koordinate der Drehmitte des Textblocks im Verhältnis zum Ursprung der Form. Die Standardformel lautet: 
  
= Höhe \* 0,5
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle TxtPinY anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtPinY  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle TxtPinY nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormPinY** <br/> |
   

