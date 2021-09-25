---
title: Zelle "SpAfter" (Abschnitt "Paragraph")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm960
ms.localizationpriority: medium
ms.assetid: 2dd56ae5-300e-ba09-a73a-83c2b6c2a0ef
description: Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, nach jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den letzten Absatz in einem Textblock handelt (die Zelle BottomMargin).
ms.openlocfilehash: cdabd57f5dbad41e9b4d09e684c59df242d1e2ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622788"
---
# <a name="spafter-cell-paragraph-section"></a>Zelle "SpAfter" (Abschnitt "Paragraph")

Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, nach jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den letzten Absatz in einem Textblock handelt (die Zelle BottomMargin).
  
## <a name="remarks"></a>Bemerkungen

Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn es sich um eine skalierte Zeichnung handelt, bleibt die Einstellung für Abstand nach unverändert.
  
Um einen Verweis auf die Zelle "SpAfter" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Para.SpAfter[  *i*  ] where  *i*  = <1>, 2, 3...  <br/> |
   
Um einen Verweis auf die Zelle "SpAfter" anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionParagraph** <br/> |
| Zeilenindex:  <br/> |**visRowParagraph**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visSpaceAfter** <br/> |
   

