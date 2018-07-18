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
ms.openlocfilehash: 57fdb320395a9a6562983a0148b37c4a70a9a9b6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797859"
---
# <a name="rightmargin-cell-text-block-format-section"></a>RightMargin Cell (Text Block Format Section)

Bestimmt den Abstand zwischen dem rechten Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt.
  
## <a name="remarks"></a>Hinweise

Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der rechte Rand unverändert.
  
Wenn Sie einen Verweis auf die Zelle RightMargin aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | RightMargin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle RightMargin aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkRightMargin** <br/> |
   

