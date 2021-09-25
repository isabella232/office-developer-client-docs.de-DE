---
title: Zelle "ExtraInfo" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm360
ms.localizationpriority: medium
ms.assetid: 55834445-8619-f79a-aea0-0f6a1780e016
description: Stellt eine Zeichenfolge dar, die Informationen für die Auflösung einer URL enthält (z. B. die Koordinaten einer Imagemap). Beispielsweise gibt x=41 y=7 in der Zelle ExtraInfo &amp; die Koordinaten einer Bildzuordnung an.
ms.openlocfilehash: 1b913c549bf11d999afb0866b9927fa5fa270be3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570652"
---
# <a name="extrainfo-cell-hyperlinks-section"></a>Zelle "ExtraInfo" (Abschnitt "Hyperlinks")

Stellt eine Zeichenfolge dar, die Informationen für die Auflösung einer URL enthält (z. B. die Koordinaten einer Imagemap). In der Zelle "ExtraInfo" gibt "x=41 &amp; y=7" beispielsweise die Koordinaten einer Bildzuordnung an.
  
## <a name="remarks"></a>HinwBemerkungeneise

Ereigniszellen werden erst beim Eintreffen des Ereignisses ausgewertet, nicht beim Eingeben der Formel.
  
Um einen Verweis auf die Zelle "ExtraInfo" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Hyperlink.  *Name*  . ExtraInfo where Hyperlink.  *Name*  ist der Zeilenname  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ExtraInfo anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
| Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i* where *i* = 0, 1, 2...  <br/> |
| Zeilenindex:  <br/> |**visHLinkExtraInfo** <br/> |
   

