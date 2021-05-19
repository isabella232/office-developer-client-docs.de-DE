---
title: Zelle "RightMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Bestimmt den Abstand zwischen dem rechten Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt.
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433521"
---
# <a name="rightmargin-cell-text-block-format-section"></a>Zelle "RightMargin" (Abschnitt "Text Block Format")

Bestimmt den Abstand zwischen dem rechten Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt.
  
## <a name="remarks"></a>Hinweise

Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der rechte Rand unverändert.
  
Um einen Verweis auf die Zelle RightMargin anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | RightMargin  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle RightMargin nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkRightMargin** <br/> |
   

