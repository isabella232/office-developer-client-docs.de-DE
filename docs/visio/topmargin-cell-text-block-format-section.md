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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435572"
---
# <a name="topmargin-cell-text-block-format-section"></a>Zelle "TopMargin" (Abschnitt "Text Block Format")

Bestimmt den Abstand zwischen dem oberen Rand des Textblocks und der ersten darin enthaltenen Textzeile. Der Standardwert beträgt 4,0000 Punkt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der obere Rand unverändert.
  
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die TopMargin-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | TopMargin  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die TopMargin-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkTopMargin** <br/> |
   

