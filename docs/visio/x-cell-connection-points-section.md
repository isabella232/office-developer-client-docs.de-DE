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
description: Stellt die X-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.
ms.openlocfilehash: 27821f9aa94f97d8e019d7c7307c036549bf807b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798428"
---
# <a name="x-cell-connection-points-section"></a>X Cell (Connection Points Section)

Stellt die *X* -Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle X nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Connections.X *i* wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
| Zeilenindex:  <br/> |**VisRowConnectionPts** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visX** <br/> |
   

