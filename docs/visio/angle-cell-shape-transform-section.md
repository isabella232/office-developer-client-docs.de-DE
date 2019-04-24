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
ms.openlocfilehash: 85f64c6111b492940d278a5558508a2dea6b1e1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341468"
---
# <a name="angle-cell-shape-transform-section"></a>Zelle "Angle" (Abschnitt "Shape Transform")

Stellt den tatsächlichen Drehwinkel des Shapes im Verhältnis zu seinem übergeordneten Objekt dar. Die Standardformel zur Bestimmung des Drehwinkels eines 1D-Shapes lautet: =ARCTAN2(EndeY-AnfangY,EndeX-AnfangX).
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Angle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Winkel  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "Angle" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormAngle** <br/> |
   

