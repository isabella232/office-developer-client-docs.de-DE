---
title: Zelle "Size" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
ms.localizationpriority: medium
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Definiert die Größe des Texts im Textblock des Shapes.
ms.openlocfilehash: bd20175567010aafd2e2a88ebdf5722032f5624e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559546"
---
# <a name="size-cell-character-section"></a>Zelle "Size" (Abschnitt "Character")

Definiert die Größe des Texts im Textblock des Shapes.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Größe des Texts ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Textgröße unverändert.
  
Um einen Verweis auf die Zelle Size anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Char.Size[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle Size anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
| Zeilenindex:  <br/> |**visRowCharacter**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visCharacterSize** <br/> |
   

