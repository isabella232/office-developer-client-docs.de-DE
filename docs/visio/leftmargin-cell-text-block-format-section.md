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
ms.openlocfilehash: d24ba33bffea1529490b49e105fec5d01cd828b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797308"
---
# <a name="leftmargin-cell-text-block-format-section"></a>LeftMargin Cell (Text Block Format Section)

Bestimmt den Abstand zwischen dem linken Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der linke Rand unverändert.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle LeftMargin nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LeftMargin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle LeftMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkLeftMargin** <br/> |
   

