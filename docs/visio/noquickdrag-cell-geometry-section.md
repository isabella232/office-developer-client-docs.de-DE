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
description: Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den durch den Abschnitt Geometrie definierten gefüllten Bereich klickt.
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341062"
---
# <a name="noquickdrag-cell-geometry-section"></a>Zelle "NoQuickDrag" (Abschnitt "Geometrie")

Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den durch den Abschnitt Geometrie definierten gefüllten Bereich klickt.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle NoQuickDrag aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Geometrie *i* . NoQuickDrag, wobei * i *-<1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle NoQuickDrag aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zeilenindex:  <br/> |**visRowComponent** <br/> |
|Zellenindex:  <br/> |**visCompNoQuickDrag** <br/> |
   

