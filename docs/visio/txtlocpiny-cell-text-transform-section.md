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
description: 'Bestimmt die y-Koordinate des Drehmittelpunkts des Textblocks relativ zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 937c4e9928d32d55e8336d192b1ecc6140fd8381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414060"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>Zelle "TxtLocPinY" (Abschnitt "Text Transform")

Bestimmt die *y* -Koordinate des Drehmittelpunkts des Textblocks relativ zum Ursprung des Textblocks. Die Standardformel lautet: 
  
= Zelle TxtHeight \* 0,5
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle TxtLocPinY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle TxtLocPinY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle TxtLocPinY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinY** <br/> |
   

