---
title: Zelle "NoLine" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm715
localization_priority: Normal
ms.assetid: f9624af2-c087-3dde-9140-339c438b3652
description: Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.
ms.openlocfilehash: 1e43072363461e6b8fcd511c70512f3bfef4504f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797541"
---
# <a name="noline-cell-geometry-section"></a>NoLine Cell (Geometry Section)

Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Es wird keine Linie um die Grenze eines Pfads gezogen, bei der es sich um die Grenze eines ausgefüllten Bereichs handelt.  <br/> |
| FALSE  <br/> | Es wird eine Linie um die Grenze eines Pfades gezogen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie die Farbe einer Linie in weiß ändern, ist diese Linie immer noch vorhanden, auch wenn sie vor einem weißen Hintergrund nicht mehr angezeigt wird. Wenn Sie in diese Zelle den Wert WAHR einsetzen, wird keine Linie gezogen.
  
Wenn Sie einen Verweis auf die Zelle NoLine aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . NoLine wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle NoLine aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zellenindex:  <br/> |**visCompNoLine** <br/> |
   

