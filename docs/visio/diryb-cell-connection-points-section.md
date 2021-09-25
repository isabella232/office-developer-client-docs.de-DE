---
title: Zelle "DirY / B" (Abschnitt "Connection Points")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
ms.localizationpriority: medium
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Bestimmt die y-Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle akzeptiert einen Fließkommawert.
ms.openlocfilehash: af2801f32533d5b82b9f3133dbc700444f04ff43
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574419"
---
# <a name="diry--b-cell-connection-points-section"></a>Zelle "DirY / B" (Abschnitt "Connection Points")

Bestimmt die  *y-Komponente*  für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts. Sie wird auch zur Ausrichtung des angefügten Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle benötigt einen Fließkommawert. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle DirY/B anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Connections.DirY[ *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle DirY/B anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
|Zeilenindex:  <br/> |**visRowConnectionPts**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCnnctDirY** (nicht erweiterte Zeilen)           **visCnnctB** (erweiterte Zeilen)  <br/> |
   
Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.
  

