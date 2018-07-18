---
title: QuickStyleFillColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Bestimmt, welche Designfarbe an, die Füllung einer Form verwendet wird, als ganze Zahl im Bereich von 0 bis 7
ms.openlocfilehash: dcbb974947821327e7cff6634fd9435f5e5845bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797761"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>QuickStyleFillColor Cell (Quick Style Section)

Bestimmt, welche Designfarbe an, die Füllung einer Form verwendet wird, als ganze Zahl im Bereich von 0 bis 7
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Der Füllfarbe einer Form erbt die Designfarbe dunkel an.  <br/> |
|1  <br/> |Der Füllfarbe einer Form erbt die Designfarbe hell an.  <br/> |
|2  <br/> |Der Füllfarbe einer Form erbt die Designfarbe Akzent 1  <br/> |
|3  <br/> |Der Füllfarbe einer Form erbt die Designfarbe Akzent 2  <br/> |
|4  <br/> |Der Füllfarbe einer Form erbt die Designfarbe Akzent 3  <br/> |
|5  <br/> |Der Füllfarbe einer Form erbt die Designfarbe Akzent 4  <br/> |
|6  <br/> |Der Füllfarbe einer Form erbt die Designfarbe Akzent 5  <br/> |
|7  <br/> |Der Füllfarbe einer Form erbt die Designfarbe Akzent 6  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **QuickStyleFillColor** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleFillColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleFillColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleFillColor** <br/> |
   

