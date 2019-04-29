---
title: Zelle "SpBefore" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm965
localization_priority: Normal
ms.assetid: a7d5b0a1-3657-8211-f0e0-eaed588fa0bc
description: Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, vor jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den ersten Absatz in einem Textblock handelt (die Zelle TopMargin).
ms.openlocfilehash: 9890910a11990bb5be7fe3ee4af95e578c8d9799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425757"
---
# <a name="spbefore-cell-paragraph-section"></a>Zelle "SpBefore" (Abschnitt "Paragraph")

Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, vor jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den ersten Absatz in einem Textblock handelt (die Zelle TopMargin).
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn es sich um eine skalierte Zeichnung handelt, bleibt die Einstellung für Abstand vor unverändert.
  
Wenn Sie einen Verweis auf die Zelle aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Abs. vor [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSpaceBefore** <br/> |
   

