---
title: QuickStyleLineColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dcfb792f-e02a-4059-acec-a178d221097c
description: Bestimmt, welche Designfarbe an, die Position einer Form verwendet wird, als ganze Zahl im Bereich von 0 bis 7.
ms.openlocfilehash: 2a660472998ade8148e8b70a3c6e4fc5fb3f4820
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797776"
---
# <a name="quickstylelinecolor-cell-quick-style-section"></a>QuickStyleLineColor Cell (Quick Style Section)

Bestimmt, welche Designfarbe an, die Position einer Form verwendet wird, als ganze Zahl im Bereich von 0 bis 7.
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Die Linienfarbe Shape erbt die Designfarbe dunkel an.  <br/> |
|1  <br/> |Die Linienfarbe Shape erbt die Designfarbe hell an.  <br/> |
|2  <br/> |Die Farbe der Form erbt die Designfarbe Akzent 1  <br/> |
|3  <br/> |Die Farbe der Form erbt die Designfarbe Akzent 2  <br/> |
|4  <br/> |Die Farbe der Form erbt die Designfarbe Akzent 3  <br/> |
|5  <br/> |Die Farbe der Form erbt die Designfarbe Akzent 4  <br/> |
|6  <br/> |Die Farbe der Form erbt die Designfarbe Akzent 5  <br/> |
|7  <br/> |Die Farbe der Form erbt die Designfarbe Akzent 6  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **QuickStyleLineColor** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleLineColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleLineColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleLineColor** <br/> |
   

