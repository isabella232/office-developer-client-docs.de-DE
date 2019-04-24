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
ms.openlocfilehash: 97d349fd4ddc3c76cda61e1ee7ce25909161e6fa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280924"
---
# <a name="topmargin-cell-text-block-format-section"></a>Zelle "TopMargin" (Abschnitt "Text Block Format")

Bestimmt den Abstand zwischen dem oberen Rand des Textblocks und der ersten darin enthaltenen Textzeile. Der Standardwert beträgt 4,0000 Punkt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der obere Rand unverändert.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle oberRand aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TopMargin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle oberRand aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkTopMargin** <br/> |
   

