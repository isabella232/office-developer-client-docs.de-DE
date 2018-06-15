---
title: QuickStyleShadowColor Cell (Quick Style Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0a80959f-941f-451c-9049-dc661ff4930f
description: Bestimmt, welche Designfarbe an, die der Schatten eines Shapes verwendet wird, als ganze Zahl im Bereich von 0 bis 7.
ms.openlocfilehash: 303a1dfe44960920a6679ea4cc85fb849f8a9cba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797764"
---
# <a name="quickstyleshadowcolor-cell-quick-style-section"></a>QuickStyleShadowColor Cell (Quick Style Section)

Bestimmt, welche Designfarbe an, die der Schatten eines Shapes verwendet wird, als ganze Zahl im Bereich von 0 bis 7.
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Die Farbe des Shape-Schattens erbt die Designfarbe dunkel an.  <br/> |
|1  <br/> |Die Farbe des Shape-Schattens erbt vom die Designfarbe hell an.  <br/> |
|2  <br/> |Die Farbe des Shape-Schattens erbt die Designfarbe Akzent 1.  <br/> |
|3  <br/> |Die Farbe des Shape-Schattens erbt vom die Designfarbe Akzent 2 an.  <br/> |
|4  <br/> |Die Farbe des Shape-Schattens erbt die Designfarbe Akzent 3 an.  <br/> |
|5  <br/> |Die Farbe des Shape-Schattens erbt die Designfarbe Akzent 4 an.  <br/> |
|6  <br/> |Die Farbe des Shape-Schattens erbt die Designfarbe Akzent 5 an.  <br/> |
|7  <br/> |Die Farbe des Shape-Schattens erbt die Designfarbe Akzent 6 an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **QuickStyleShadowColor** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleShadowColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleShadowColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleShadowColor** <br/> |
   

