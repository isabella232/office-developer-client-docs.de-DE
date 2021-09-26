---
title: Zelle "SortKey" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
ms.localizationpriority: medium
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.
ms.openlocfilehash: 1bf3a5f77905f130a37d911550411343747b803d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603466"
---
# <a name="sortkey-cell-hyperlinks-section"></a>Zelle "SortKey" (Abschnitt "Hyperlinks")

Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Hyperlinks in Kontextmenüs werden von unten nach oben sortiert, wobei die Hyperlinks mit der kleinsten Nummer im Menü an oberster Stelle angezeigt werden. Wenn zwei Hyperlinks für die Zelle SortKey denselben Wert aufweisen, wird die Reihenfolge durch die physische Zeilenreihenfolge bestimmt. Der Standardwert ist 0 (Null). 
  
Verwenden Sie zum Abrufen eines Verweises auf die Zelle SortKey anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name*  . SortKey, wobei Hyperlink  *.name*  der Zeilenname ist  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle SortKey anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
|Zeilenindex:  <br/> |**visRow1stHyperlink**  +   *i* where *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visHLinkSortKey** <br/> |
   

