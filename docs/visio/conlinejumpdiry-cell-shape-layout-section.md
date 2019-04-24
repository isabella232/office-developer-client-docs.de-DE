---
title: Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251654
localization_priority: Normal
ms.assetid: 93f82ae0-3442-fac1-9906-b84afef85f5c
description: Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.
ms.openlocfilehash: f86c77da62042d1bc2c0274564efa9fdb0887971
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342742"
---
# <a name="conlinejumpdiry-cell-shape-layout-section"></a>Zelle "ConLineJumpDirY" (Abschnitt "Shape Layout")

Bestimmt die Liniensprungrichtung für Liniensprünge, die bei einem vertikalen dynamischen Verbinder für ein Shape auftreten.
  
|**Wert**|**Liniensprungrichtung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Zeichenblattstandard  <br/> |**visLOJumpDirYDefault** <br/> |
| 1  <br/> | Nach links  <br/> |**visLOJumpDirYLeft** <br/> |
| 2  <br/> | Nach rechts  <br/> |**visLOJumpDirYRight** <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie die standardmäßige vertikale Richtung für *alle* Verbinder-Sprünge auf einer Seite festlegen möchten, verwenden Sie die Zelle Zelle PageLineJumpDirY im Abschnitt Seiten Layout. 
  
Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpDirY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle ConLineJumpDirY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle ConLineJumpDirY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowShapeLayout** <br/> |
| Zellenindex:  <br/> |**visSLOJumpDirY** <br/> |
   

