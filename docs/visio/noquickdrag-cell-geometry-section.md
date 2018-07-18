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
description: Bestimmt, ob ein Shape ausgewählt oder gezogen werden, wenn der Benutzer den vom Abschnitt "Geometrie" definierten ausgefüllten Bereich klickt werden kann.
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797555"
---
# <a name="noquickdrag-cell-geometry-section"></a>NoQuickDrag Cell (Geometry Section)

Bestimmt, ob ein Shape ausgewählt oder gezogen werden, wenn der Benutzer den vom Abschnitt "Geometrie" definierten ausgefüllten Bereich klickt werden kann.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie eine Referenz auf die Zelle NoQuickDrag aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes. 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Geometrie *i* . NoQuickDrag, wobei * ich * - < 1 >, 2, 3...  <br/> |
   
Wenn Sie eine Referenz auf die Zelle NoQuickDrag aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**VisSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zeilenindex:  <br/> |**visRowComponent** <br/> |
|Zellenindex:  <br/> |**visCompNoQuickDrag** <br/> |
   

