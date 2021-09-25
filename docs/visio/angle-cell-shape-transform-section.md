---
title: Zelle "Angle" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251196
ms.localizationpriority: medium
ms.assetid: d05a001c-9001-90d9-5028-f38b90acc53e
description: 'Stellt den tatsächlichen Drehwinkel des Shapes im Verhältnis zu seinem übergeordneten Objekt dar. Die Standardformel zur Bestimmung des Drehwinkels eines 1D-Shapes lautet: =ARCTAN2(EndeY-AnfangY,EndeX-AnfangX).'
ms.openlocfilehash: 0e4beb3ce83623580cd7fabcfdb788121ff1ba46
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560123"
---
# <a name="angle-cell-shape-transform-section"></a>Zelle "Angle" (Abschnitt "Shape Transform")

Stellt den tatsächlichen Drehwinkel des Shapes im Verhältnis zu seinem übergeordneten Objekt dar. Die Standardformel zur Bestimmung des Drehwinkels eines 1D-Shapes lautet: =ARCTAN2(EndeY-AnfangY,EndeX-AnfangX).
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle Angle anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Winkel  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Angle anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormAngle** <br/> |
   

