---
title: Zelle "ExtraInfo" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
localization_priority: Normal
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Stellt eine Zeichenfolge, die Informationen für die Auflösung einer URL, beispielsweise die Koordinaten einer Imagemap übergibt. Beispielsweise in die Zelle ExtraInfo X = 41&amp;y = 7specifies die Koordinaten einer Imagemap.
ms.openlocfilehash: aa035d5ec863cd8045063af970efa26b53683793
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796978"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>ExtraInfo Cell (Hyperlinks Section)

Stellt eine Zeichenfolge, die Informationen für die Auflösung einer URL, beispielsweise die Koordinaten einer Imagemap übergibt. Beispielsweise in die Zelle ExtraInfo "X = 41&amp;y = 7" gibt die Koordinaten einer Imagemap an.
  
## <a name="remarks"></a>Hinweise

Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.
  
Wenn Sie einen Verweis auf die Zelle ExtraInfo nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name* . ExtraInfo, in dem Hyperlink.  *Name* ist der Zeilenname  <br/> |
   
Wenn Sie einen Verweis auf die Zelle ExtraInfo aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* wobei *i* = 0, 1, 2...  <br/> |
| Zellenindex:  <br/> |**visHLinkExtraInfo** <br/> |
   

