---
title: Zelle "BottomMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm120
localization_priority: Normal
ms.assetid: 3121911b-34d5-d99c-3806-76f6e2824f92
description: Bestimmt den Abstand zwischen dem unteren Rand des Textblocks und der letzten darin enthaltenen Textzeile. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Größe der Zeichnung verändert wird, bleibt der untere Rand gleich.
ms.openlocfilehash: f3515485b0418ffeaf55910a972e1e480f428e4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796547"
---
# <a name="bottommargin-cell-text-block-format-section"></a>BottomMargin Cell (Text Block Format Section)

Bestimmt den Abstand zwischen dem unteren Rand des Textblocks und der letzten darin enthaltenen Textzeile. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Größe der Zeichnung verändert wird, bleibt der untere Rand gleich.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle BottomMargin aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BottomMargin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle BottomMargin aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkBottomMargin** <br/> |
   

