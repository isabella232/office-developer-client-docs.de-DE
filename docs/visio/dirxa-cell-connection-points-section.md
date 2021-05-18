---
title: Zelle "DirX / A" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Bestimmt die x-Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Die Zelle DirX/A wird auch verwendet, um das angefügte Bein eines dynamischen Verbinders zu orientieren. Diese Zelle akzeptiert einen Fließkommawert.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422397"
---
# <a name="dirx--a-cell-connection-points-section"></a>Zelle "DirX / A" (Abschnitt "Connection Points")

Bestimmt die  *x-Komponente*  für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Die Zelle DirX/A wird auch verwendet, um das angefügte Bein eines dynamischen Verbinders zu orientieren. Diese Zelle benötigt einen Fließkommawert. 
  
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle DirX/A anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Connections.DirX[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DirX/A nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
| Zeilenindex:  <br/> |**visRowConnectionPts**  +   *i* where *i* = 0, 1, 2  <br/> |
| Zellenindex:  <br/> |**visCnnctDirX** (nicht erweiterte Zeilen)           **visCnnctA** (erweiterte Zeilen)  <br/> |
   
Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.
  

