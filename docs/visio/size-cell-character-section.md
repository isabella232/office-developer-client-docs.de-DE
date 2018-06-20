---
title: Zelle "Size" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Definiert die Größe des Texts im Textblock des Shapes.
ms.openlocfilehash: f3077441844b859cf224eccc8180d0d56cce851f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798120"
---
# <a name="size-cell-character-section"></a>Size Cell (Character Section)

Definiert die Größe des Texts im Textblock des Shapes.
  
## <a name="remarks"></a>Hinweise

Die Größe des Texts ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Textgröße unverändert.
  
Wenn Sie einen Verweis auf die Zelle Size nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Char.Size [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Size aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
| Zeilenindex:  <br/> |**VisRowCharacter** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCharacterSize** <br/> |
   

