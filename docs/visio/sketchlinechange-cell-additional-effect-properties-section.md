---
title: Zelle "SketchLineChange" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Bestimmt die Zufälligkeit der Linie des Shapes anhand der Geometrie des Shapes bei Verwendung eines Skizzeneffekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle SketchLineChange auf 0 % festgelegt ist, entspricht die Geometrie der Linie des Shapes der Geometrie des Shapes. Wenn der Wert 100 % ist, entspricht die Geometrie der Linie des Shapes nicht der Geometrie des Shapes.
ms.openlocfilehash: 39a5726354ac350e289e6b114f3c1664d2a1aeae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549581"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>Zelle "SketchLineChange" (Abschnitt "Additional Effect Properties")

Bestimmt die Zufälligkeit der Linie des Shapes anhand der Geometrie des Shapes bei Verwendung eines Skizzeneffekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle **SketchLineChange** auf 0 % festgelegt ist, entspricht die Geometrie der Linie des Shapes der Geometrie des Shapes. Wenn der Wert 100 % ist, entspricht die Geometrie der Linie des Shapes nicht der Geometrie des Shapes. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Für optimale Ergebnisse liegt der ideale Wertebereich für die Zelle **SketchLineChange** zwischen 15 % und 50 %. Ein Wert unter 15 % ist wahrnehmbar. Ein Wert größer als 50 % könnte die Zeile zu sehr zufälligisieren. 
  
Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "SketchLineChange"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchLineChange  <br/> |
   
Um einen Verweis auf die Zelle **"SketchLineChange"** anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchLineChange** <br/> |
   

