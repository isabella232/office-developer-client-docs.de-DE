---
title: Zelle "DirY / B" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Bestimmt die y-Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle akzeptiert einen Fließkommawert.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417091"
---
# <a name="diry--b-cell-connection-points-section"></a>Zelle "DirY / B" (Abschnitt "Connection Points")

Bestimmt die  *y-Komponente*  für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle benötigt einen Fließkommawert. 
  
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle DirY/B anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Connections.DirY[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DirY/B nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
|Zeilenindex:  <br/> |**visRowConnectionPts**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCnnctDirY** (nicht erweiterte Zeilen)           **visCnnctB** (erweiterte Zeilen)  <br/> |
   
Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.
  

