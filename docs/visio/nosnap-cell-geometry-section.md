---
title: Zelle "NoSnap" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: Definiert, ob andere Shapes an einem Pfad einrasten.
ms.openlocfilehash: 60a6532aee0f391eb38609f6ed87577e5558d5c2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341131"
---
# <a name="nosnap-cell-geometry-section"></a>Zelle "NoSnap" (Abschnitt "Geometry")

Definiert, ob andere Shapes an einem Pfad einrasten.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Andere Shapes können nicht an diesem Pfad einrasten.  <br/> |
| FALSE  <br/> | Andere Shapes können an diesem Pfad einrasten.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle noSnap aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . NoSnap, wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle noSnap aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowComponent** <br/> |
| Zeilenindex:  <br/> |**visCompNoSnap** <br/> |
   

