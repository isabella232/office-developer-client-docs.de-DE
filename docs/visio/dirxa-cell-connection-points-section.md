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
description: Legt die X-Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts. Die Zelle DirX / eine Zelle wird auch verwendet, um die Ausrichtung des verbundenen Abschnitts eines dynamischen Verbinders. Diese Zelle benötigt einen Gleitkommawert Codepunktwert.
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796869"
---
# <a name="dirx--a-cell-connection-points-section"></a>DirX / A Cell (Connection Points Section)

Legt die *X* -Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts. Die Zelle DirX / eine Zelle wird auch verwendet, um die Ausrichtung des verbundenen Abschnitts eines dynamischen Verbinders. Diese Zelle benötigt einen Gleitkommawert Codepunktwert. 
  
## <a name="remarks"></a>Hinweise

Einen Verweis auf die Zelle DirX / eine Zelle nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft verwenden: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Verbindungen.RichtX [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Einen Verweis auf die Zelle DirX / eine Zelle aus einem Programm nach Index verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionConnectionPts** <br/> |
| Zeilenindex:  <br/> |**VisRowConnectionPts** +  *i* wobei *i* = 0, 1, 2  <br/> |
| Zellenindex:  <br/> |**visCnnctDirX** (nicht erweiterte Zeilen)           **visCnnctA** (erweiterte Zeilen)  <br/> |
   
Informationen zu erweiterten und nicht erweiterten Zeilen finden Sie in der Zeile Connections Points.
  

