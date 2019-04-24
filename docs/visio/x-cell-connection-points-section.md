---
title: Zelle "X" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Stellt die x-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.
ms.openlocfilehash: 496e5af6ea5b7ba99730b23dcbb510db6af9b23b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339879"
---
# <a name="x-cell-connection-points-section"></a>Zelle "X" (Abschnitt "Connection Points")

Stellt die *x* -Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Connections. X *i* Where *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
| Zeilenindex:  <br/> |**visRowConnectionPts** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visX** <br/> |
   

