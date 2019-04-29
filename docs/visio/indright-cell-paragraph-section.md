---
title: Zelle "IndRight" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251256
localization_priority: Normal
ms.assetid: f0891064-95d9-ae1b-28f3-3aef1406b636
description: Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom rechten Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der rechte Einzug gleich.
ms.openlocfilehash: e6529bf41cb8fdd40371d9a663291961626afb56
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408866"
---
# <a name="indright-cell-paragraph-section"></a>Zelle "IndRight" (Abschnitt "Paragraph")

Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom rechten Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der rechte Einzug gleich.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle IndRight aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Abs. IndRight [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle IndRight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visIndentRight** <br/> |
   

