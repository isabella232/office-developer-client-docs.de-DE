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
description: Stellt die X-der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung seines übergeordneten-Koordinate.
ms.openlocfilehash: 74e98732f1e0c44fa20c159070198ed4f98cee92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797606"
---
# <a name="pinx-cell-shape-transform-section"></a>PinX Cell (Shape Transform Section)

Stellt die *X* -der Drehbezugspunkts (Drehmittelpunkts) im Verhältnis zum Ursprung seines übergeordneten-Koordinate. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle PinX aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | PinX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle PinX aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormPinX** <br/> |
   

