---
title: QuickStyleShadowColor Cell (Quick Style section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0a80959f-941f-451c-9049-dc661ff4930f
description: Bestimmt die Design Farbe, die der Schatten eines Shapes verwendet, als ganze Zahl zwischen 0 und 7.
ms.openlocfilehash: b623eee89d214bade2706b12fcb344eccd8814b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360038"
---
# <a name="quickstyleshadowcolor-cell-quick-style-section"></a>QuickStyleShadowColor Cell (Quick Style section)

Bestimmt die Design Farbe, die der Schatten eines Shapes verwendet, als ganze Zahl zwischen 0 und 7.
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Die Form Schattenfarbe erbt von der dunklen Design Farbe.  <br/> |
|1  <br/> |Die Form Schattenfarbe erbt von der Farbe des hellen Designs.  <br/> |
|2  <br/> |Die Form Schattenfarbe erbt von der Design Farbe Akzent 1.  <br/> |
|3  <br/> |Die Schattenfarbe des Shapes erbt von der Design Farbe Akzent 2.  <br/> |
|4  <br/> |Die Schattenfarbe des Shapes erbt von der Design Farbe Akzent 3.  <br/> |
|5  <br/> |Die Schattenfarbe des Shapes erbt von der Design Farbe Akzent 4.  <br/> |
|6  <br/> |Die Schattenfarbe des Shapes erbt von der Design Farbe Akzent 5.  <br/> |
|7  <br/> |Die Schattenfarbe des Shapes erbt von der Design Farbe Akzent 6.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **QuickStyleShadowColor** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleShadowColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleShadowColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleShadowColor** <br/> |
   

