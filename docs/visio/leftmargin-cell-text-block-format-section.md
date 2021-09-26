---
title: Zelle "LeftMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251265
ms.localizationpriority: medium
ms.assetid: 47d84d7d-08a0-1934-d156-702da848e01c
description: Bestimmt den Abstand zwischen dem linken Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der linke Rand unverändert.
ms.openlocfilehash: 57dcc1a0b99a8fc3d2a205555ccbee5520b1dac7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618679"
---
# <a name="leftmargin-cell-text-block-format-section"></a>Zelle "LeftMargin" (Abschnitt "Text Block Format")

Bestimmt den Abstand zwischen dem linken Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der linke Rand unverändert.
  
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle "LeftMargin" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LeftMargin  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LeftMargin anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkLeftMargin** <br/> |
   

