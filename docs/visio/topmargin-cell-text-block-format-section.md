---
title: Zelle "TopMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1015
localization_priority: Normal
ms.assetid: c599b444-4d0e-a855-b04b-dd9dcaedf263
description: Bestimmt den Abstand zwischen dem oberen Rand des Textblocks und der ersten darin enthaltenen Textzeile. Der Standardwert beträgt 4,0000 Punkt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der obere Rand unverändert.
ms.openlocfilehash: 71e8e3b41dc9c59c374111dcd442e55ab70330fa
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798307"
---
# <a name="topmargin-cell-text-block-format-section"></a>Zelle "TopMargin" (Abschnitt "Text Block Format")

Bestimmt den Abstand zwischen dem oberen Rand des Textblocks und der ersten darin enthaltenen Textzeile. Der Standardwert beträgt 4,0000 Punkt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der obere Rand unverändert.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle TopMargin nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TopMargin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle TopMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkTopMargin** <br/> |
   

