---
title: Zelle "PinY" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm795
localization_priority: Normal
ms.assetid: 98b86b9d-9cc0-1169-1c44-ef1505bf92fa
description: Stellt die y-Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung des übergeordneten Elements dar.
ms.openlocfilehash: 17daf691e4802a93775bfd5272d2142ef33bd189
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411862"
---
# <a name="piny-cell-shape-transform-section"></a>Zelle "PinY" (Abschnitt "Shape Transform")

Stellt die *y* -Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung des übergeordneten Elements dar. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle PinY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PinY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PinY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormPinY** <br/> |
   

