---
title: Zelle "FlipX" (Abschnitt "Shape Transform")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251197
localization_priority: Normal
ms.assetid: 8d4f5e14-4f17-05a6-4092-5a102c9dc85f
description: Gibt an, ob das Shape horizontal gekippt wurde.
ms.openlocfilehash: fc014ff6c5a3650361d6afd478a5858f84fb5c47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797035"
---
# <a name="flipx-cell-shape-transform-section"></a>FlipX Cell (Shape Transform Section)

Gibt an, ob das Shape horizontal gekippt wurde.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Das Shape wurde horizontal gekippt.  <br/> |
| FALSE  <br/> | Das Shape wurde nicht horizontal gekippt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle FlipX nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | FlipX  <br/> |
   
Wenn Sie einen Verweis auf die Zelle FlipX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowXFormOut** <br/> |
| Zellenindex:  <br/> |**visXFormFlipX** <br/> |
   

