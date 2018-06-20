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
description: 'Legt die y--Koordinate des Textblocks des Drehung relativ zum Ursprung des Textblocks. Die Standardformel lautet:'
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798322"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>TxtLocPinY Cell (Text Transform Section)

Legt die *y* --Koordinate des Textblocks des Drehung relativ zum Ursprung des Textblocks. Die Standardformel lautet: 
  
= TxtHeight \* 0,5
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle TxtLocPinY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtLocPinY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TxtLocPinY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormLocPinY** <br/> |
   

