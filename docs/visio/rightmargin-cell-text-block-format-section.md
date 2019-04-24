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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326775"
---
# <a name="rightmargin-cell-text-block-format-section"></a>Zelle "RightMargin" (Abschnitt "Text Block Format")

Bestimmt den Abstand zwischen dem rechten Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt.
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der rechte Rand unverändert.
  
Wenn Sie einen Verweis auf die Zelle RightMargin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | RightMargin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle RightMargin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkRightMargin** <br/> |
   

