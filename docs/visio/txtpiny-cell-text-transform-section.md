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
description: 'Legt die y--Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet:'
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798330"
---
# <a name="txtpiny-cell-text-transform-section"></a>TxtPinY Cell (Text Transform Section)

Legt die *y* --Koordinate des Textblocks des Drehung im Verhältnis zum Ursprung des Shapes. Die Standardformel lautet: 
  
= Höhe \* 0,5
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle TxtPinY nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TxtPinY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TxtPinY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowTextXForm** <br/> |
| Zellenindex:  <br/> |**visXFormPinY** <br/> |
   

