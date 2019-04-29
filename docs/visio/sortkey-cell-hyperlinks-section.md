---
title: Zelle "SortKey" (Abschnitt "Hyperlinks")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406381"
---
# <a name="sortkey-cell-hyperlinks-section"></a>Zelle "SortKey" (Abschnitt "Hyperlinks")

Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.
  
## <a name="remarks"></a>Bemerkungen

Die Hyperlinks in Kontextmenüs werden von unten nach oben sortiert, wobei die Hyperlinks mit der kleinsten Nummer im Menü an oberster Stelle angezeigt werden. Wenn zwei Hyperlinks für die Zelle SortKey denselben Wert aufweisen, wird die Reihenfolge durch die physische Zeilenreihenfolge bestimmt. Der Standardwert ist 0 (Null). 
  
Wenn Sie einen Verweis auf die Zelle SortKey aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Hyperlink. *Name* . SortKey, wobei Hyperlink *. Name* der Zeilenname ist  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "SortKey" aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionHyperlink** <br/> |
|Zeilenindex:  <br/> |**visRow1stHyperlink** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visHLinkSortKey** <br/> |
   

