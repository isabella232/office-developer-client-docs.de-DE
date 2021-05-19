---
title: Zelle "Position" (Abschnitt "Tabs")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251755
localization_priority: Normal
ms.assetid: 40d7e38e-b3b0-8616-ed27-1f963a841e03
description: Definiert die Position eines Tabstopps. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Tabstoppposition unverändert.
ms.openlocfilehash: ef17b38d708103ca004594ba04ff5b8d1ada13bf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409930"
---
# <a name="position-cell-tabs-section"></a>Zelle "Position" (Abschnitt "Tabs")

Definiert die Position eines Tabstopps. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung maßstäblich ist, bleibt die Tabstoppposition unverändert.
  
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle Position anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Registerkarten.  *ij,*            *wobei i*  und  *j*  = <1>, 2, 3...  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Position nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionTab** <br/> |
| Zeilenindex:  <br/> |**visRowTab**  +   *i,* *wobei i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> | (*j*  *3) + **visTabPos** <br/> |
   

