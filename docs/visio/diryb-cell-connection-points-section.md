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
description: Legt die y-Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts. Es wird auch zum Ausrichten des verbundenen Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle benötigt einen Gleitkommawert Codepunktwert.
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796840"
---
# <a name="diry--b-cell-connection-points-section"></a>Zelle "DirY / B" (Abschnitt "Connection Points")

Legt die *y* -Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts. Es wird auch zum Ausrichten des verbundenen Abschnitts eines dynamischen Verbinders verwendet. Diese Zelle benötigt einen Gleitkommawert Codepunktwert. 
  
## <a name="remarks"></a>Hinweise

Einen Verweis auf die Zelle DirY / B-Zelle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft verwenden: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Connections.DirY [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Einen Verweis auf die Zelle DirY / B heraus aus einem Programm nach Index verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
|Zeilenindex:  <br/> |**VisRowConnectionPts** +  *i* wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCnnctDirY** (nicht erweiterte Zeilen)           **visCnnctB** (erweiterte Zeilen)  <br/> |
   
Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.
  

