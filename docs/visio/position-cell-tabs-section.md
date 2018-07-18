---
title: Zelle "Position" (Abschnitt "Tabs")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Definiert die Position eines Tabstopps. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Tabstoppposition unverändert.
ms.openlocfilehash: 06f3a9fd5cfdf78f5383e70f32f8514b0adab114
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797727"
---
# <a name="position-cell-tabs-section"></a>Zelle "Position" (Abschnitt "Tabs")

Definiert die Position eines Tabstopps. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Tabstoppposition unverändert.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle Position aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Registerkarten.  *Ij* wobei *i* und *j* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Position aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTab** <br/> |
| Zeilenindex:  <br/> |**VisRowTab** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> | (*j* * 3) + **VisTabPos** <br/> |
   

