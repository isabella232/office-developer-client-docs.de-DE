---
title: Zelle "Angle" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
localization_priority: Normal
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Stellt den tatsächlichen Drehwinkel des Shapes im Verhältnis zu seinem übergeordneten Objekt dar. Die Standardformel zur Bestimmung des Drehwinkels eines 1D-Shapes lautet: =ARCTAN2(EndeY-AnfangY,EndeX-AnfangX).'
ms.openlocfilehash: ff052c5b254f9b49a97f5d362a4643e16a27b85d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796391"
---
# <a name="angle-cell-shape-transform-section"></a>Angle Cell (Shape Transform Section)

Stellt den tatsächlichen Drehwinkel des Shapes im Verhältnis zu seinem übergeordneten Objekt dar. Die Standardformel zur Bestimmung des Drehwinkels eines 1D-Shapes lautet: =ARCTAN2(EndeY-AnfangY,EndeX-AnfangX).
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Angle aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Angle  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Angle aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormAngle** <br/> |
   

