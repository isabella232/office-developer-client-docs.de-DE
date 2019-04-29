---
title: Zelle "PinX" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm790
localization_priority: Normal
ms.assetid: dd88fb8d-3ec3-476a-870d-6642b191496f
description: Stellt die x-Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung des übergeordneten Elements dar.
ms.openlocfilehash: de12b379d5f345209a468298174634ff4f9cd639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404820"
---
# <a name="pinx-cell-shape-transform-section"></a>Zelle "PinX" (Abschnitt "Shape Transform")

Stellt die *x* -Koordinate der PIN des Shapes (Drehmittelpunkt) im Verhältnis zum Ursprung des übergeordneten Elements dar. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle PinX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PinX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PinX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormPinX** <br/> |
   

