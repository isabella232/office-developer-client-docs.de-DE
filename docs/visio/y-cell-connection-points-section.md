---
title: Zelle "Y" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
ms.localizationpriority: medium
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Stellt die y-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.
ms.openlocfilehash: cceced17d52a847a5b1d2fb96e7995a1e543aaad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553550"
---
# <a name="y-cell-connection-points-section"></a>Zelle "Y" (Abschnitt "Connection Points")

Stellt  die y-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle Y anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Connections.Y  *i*            where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
| Zeilenindex:  <br/> |**visRowConnectionPts**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**Visy** <br/> |
   

