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
ms.openlocfilehash: 544557f1e797315619bc9975db0b87a09981726c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417210"
---
# <a name="bottommargin-cell-text-block-format-section"></a>Zelle "BottomMargin" (Abschnitt "Text Block Format")

Bestimmt den Abstand zwischen dem unteren Rand des Textblocks und der letzten darin enthaltenen Textzeile. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Größe der Zeichnung verändert wird, bleibt der untere Rand gleich.
  
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die BottomMargin-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | BottomMargin  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die BottomMargin-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkBottomMargin** <br/> |
   

