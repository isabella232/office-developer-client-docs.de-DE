---
title: Zelle "HAlign" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Definiert die horizontale Ausrichtung des Texts im Textblock des Shapes.
ms.openlocfilehash: 224e495e8aea70c418a0ab7f5a7d56975d9868e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797139"
---
# <a name="halign-cell-paragraph-section"></a>Zelle "HAlign" (Abschnitt "Paragraph")

Definiert die horizontale Ausrichtung des Texts im Textblock des Shapes.
  
|**Wert**|**Beschreibung**|**Automatisierungskonstante**|
|:-----|:-----|:-----|
| 0  <br/> | Linksbündig  <br/> |**visHorzLeft** <br/> |
| 1  <br/> | Mittig  <br/> |**visHorzCenter** <br/> |
| 2  <br/> | Rechtsbündig  <br/> |**visHorzRight** <br/> |
| 3  <br/> | Blocksatz  <br/> |**visHorzJustify** <br/> |
| 4  <br/> | Blocksatz erzwingen  <br/> |**visHorzForce** <br/> |
   
## <a name="remarks"></a>Hinweise

Beim Blocksatz wird Platz zwischen den Wörtern in jeder Zeile (nicht in der letzten Zeile) des Absatzes geschaffen, um sowohl die rechte als auch die linke Seite von Text an den Seitenrändern auszurichten.
  
Bei Blocksatz erzwingen wird jede Zeile im Absatz ausgerichtet, einschließlich der letzten Zeile.
  
Wenn Sie einen Verweis auf die Zelle HAlign aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.HorzAlign [ *i* ] wobei *i* = < 1 >, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle HAlign aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**VisRowParagraph** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHorzAlign** <br/> |
   

