---
title: Zelle "NoQuickDrag" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den gefüllten Bereich klickt, der durch den Abschnitt Geometry definiert ist.
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417721"
---
# <a name="noquickdrag-cell-geometry-section"></a>Zelle "NoQuickDrag" (Abschnitt "Geometrie")

Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den gefüllten Bereich klickt, der durch den Abschnitt Geometry definiert ist.
  
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die Zelle NoQuickDrag anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Geometry  *i*  . NoQuickDrag, wobei * i * - <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle NoQuickDrag nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionFirstComponent**  +   *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zeilenindex:  <br/> |**visRowComponent** <br/> |
|Zellenindex:  <br/> |**visCompNoQuickDrag** <br/> |
   

