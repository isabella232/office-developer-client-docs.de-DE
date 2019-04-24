---
title: Zelle "E" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251761
localization_priority: Normal
ms.assetid: bc0154b1-6930-1fe0-655c-05eab2d60230
description: Enthält die Formel eines nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-Spline, NURBS).
ms.openlocfilehash: 5c9b3cbf96e2a218a8ed790d3a5615843360c95e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327391"
---
# <a name="e-cell-geometry-section"></a>Zelle "E" (Abschnitt "Geometry")

Enthält die Formel eines nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-Spline, NURBS).
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle E aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Geometrie *i* . E *j* wobei *i* und *j* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle E nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visRowVertex** +  *j* = ** 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visNURBSData** <br/> |
   

