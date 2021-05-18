---
title: Zelle "LeftMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
localization_priority: Normal
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Bestimmt den Abstand zwischen dem linken Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der linke Rand unverändert.
ms.openlocfilehash: fee8eca8b5730e40518babe0c76549e10bebd902
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411337"
---
# <a name="leftmargin-cell-text-block-format-section"></a>Zelle "LeftMargin" (Abschnitt "Text Block Format")

Bestimmt den Abstand zwischen dem linken Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der linke Rand unverändert.
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle LeftMargin anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LeftMargin  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LeftMargin nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkLeftMargin** <br/> |
   

