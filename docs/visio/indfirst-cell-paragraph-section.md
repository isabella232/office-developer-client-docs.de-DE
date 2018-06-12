---
title: Zelle "IndFirst" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251254
localization_priority: Normal
ms.assetid: 0f2e362a-3ace-787d-6326-b5bf707f0727
description: Stellt den Abstand dar, den die erste Zeile jedes einzelnen Absatzes im Textblock des Shapes vom linken Einzug des Absatzes eingezogen ist. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der Einzug der ersten Zeile gleich.
ms.openlocfilehash: 03c34a0ccd1681d3523d743ebfc34af7b9dcfa87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797192"
---
# <a name="indfirst-cell-paragraph-section"></a>Zelle "IndFirst" (Abschnitt "Paragraph")

Stellt den Abstand dar, den die erste Zeile jedes einzelnen Absatzes im Textblock des Shapes vom linken Einzug des Absatzes eingezogen ist. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der Einzug der ersten Zeile gleich.
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle IndFirst nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.IndFirst [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle IndFirst aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visIndentFirst** <br/> |
   

