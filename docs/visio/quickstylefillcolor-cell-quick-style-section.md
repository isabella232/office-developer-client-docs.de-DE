---
title: QuickStyleFillColor Cell (Quick Style section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Bestimmt die Design Farbe, die von der Füllung eines Shapes verwendet wird, als ganze Zahl zwischen 0 und 7.
ms.openlocfilehash: 3ace0de7e3bfc878a2101eaca3847ef079b8f919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407963"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>QuickStyleFillColor Cell (Quick Style section)

Bestimmt die Design Farbe, die von der Füllung eines Shapes verwendet wird, als ganze Zahl zwischen 0 und 7.
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Die Farbe der Formfüllung erbt von der dunklen Design Farbe.  <br/> |
|1  <br/> |Die Farbe der Formfüllung erbt von der Farbe des hellen Designs.  <br/> |
|2  <br/> |Die Farbe der Formfüllung erbt von der Design Farbe Akzent 1.  <br/> |
|3  <br/> |Die Farbe der Formfüllung erbt von der Design Farbe Akzent 2.  <br/> |
|4  <br/> |Die Farbe der Formfüllung erbt von der Design Farbe Akzent 3.  <br/> |
|5  <br/> |Die Farbe der Formfüllung erbt von der Design Farbe Akzent 4.  <br/> |
|6  <br/> |Die Farbe der Formfüllung erbt von der Design Farbe Akzent 5.  <br/> |
|7  <br/> |Die Farbe der Formfüllung erbt von der Design Farbe Akzent 6.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **QuickStyleFillColor** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleFillColor  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **QuickStyleFillColor** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleFillColor** <br/> |
   

