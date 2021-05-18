---
title: Zelle QuickStyleFillColor (Abschnitt "Quick Style")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 41250e47-404c-40e7-99be-9bb8c1ed5ba2
description: Bestimmt, welche Designfarbe von der Füllung eines Shapes als ganze Zahl von 0 bis 7 verwendet wird.
ms.openlocfilehash: 3ace0de7e3bfc878a2101eaca3847ef079b8f919
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407963"
---
# <a name="quickstylefillcolor-cell-quick-style-section"></a>Zelle QuickStyleFillColor (Abschnitt "Quick Style")

Bestimmt, welche Designfarbe von der Füllung eines Shapes als ganze Zahl von 0 bis 7 verwendet wird.
  
|||
|:-----|:-----|
|Wert  <br/> |Beschreibung  <br/> |
|0  <br/> |Die Füllfarbe der Form erbt von der Dunklen Designfarbe.  <br/> |
|1  <br/> |Die Füllfarbe der Form erbt von der Farbe des Light-Designs.  <br/> |
|2  <br/> |Die Farbe der Formfüllung erbt von der Akzent 1-Designfarbe  <br/> |
|3  <br/> |Die Farbe der Formfüllung erbt von der Akzent 2-Designfarbe  <br/> |
|4   <br/> |Die Farbe der Formfüllung erbt von der Akzent 3-Designfarbe  <br/> |
|5   <br/> |Die Farbe der Formfüllung erbt von der Akzent 4-Designfarbe  <br/> |
|6   <br/> |Die Farbe der Formfüllung erbt von der Akzent 5-Designfarbe  <br/> |
|7   <br/> |Die Farbe der Formfüllung erbt von der Akzent 6-Designfarbe  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **QuickStyleFillColor-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | QuickStyleFillColor  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **QuickStyleFillColor-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowQuickStyleProperties** <br/> |
| Zellenindex:  <br/> |**visQuickStyleFillColor** <br/> |
   

