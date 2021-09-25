---
title: Zelle "RightMargin" (Abschnitt "Text Block Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
ms.localizationpriority: medium
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Bestimmt den Abstand zwischen dem rechten Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt.
ms.openlocfilehash: 4152c76a1950c598cbd979209d7a9967d11ce170
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559640"
---
# <a name="rightmargin-cell-text-block-format-section"></a>Zelle "RightMargin" (Abschnitt "Text Block Format")

Bestimmt den Abstand zwischen dem rechten Rand des Textblocks und dem darin enthaltenen Text. Standardmäßig sind 2,54 mm festgelegt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt der rechte Rand unverändert.
  
Um einen Verweis auf die Zelle "RightMargin" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | RightMargin  <br/> |
   
Um einen Verweis auf die Zelle "RightMargin" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowText** <br/> |
| Zellenindex:  <br/> |**visTxtBlkRightMargin** <br/> |
   

