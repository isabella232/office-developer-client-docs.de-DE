---
title: Zelle "SketchFillChange" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Bestimmt die Zufälligkeit der Füllung des Shapes anhand der Geometrie des Shapes bei Verwendung eines Skizzeneffekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle SketchFillChange auf 0 % festgelegt ist, entspricht die Begrenzungsgeometrie der Füllung eines Shapes der Geometrie des Shapes. Wenn der Wert 100 % ist, entspricht die Begrenzungsgeometrie der Füllung des Shapes nicht der Geometrie des Shapes.
ms.openlocfilehash: 8f3b566743c650f930a3c0163e89bfe32b77cabb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598031"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>Zelle "SketchFillChange" (Abschnitt "Additional Effect Properties")

Bestimmt die Zufälligkeit der Füllung des Shapes anhand der Geometrie des Shapes bei Verwendung eines Skizzeneffekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle **SketchFillChange** auf 0 % festgelegt ist, entspricht die Begrenzungsgeometrie der Füllung eines Shapes der Geometrie des Shapes. Wenn der Wert 100 % ist, entspricht die Begrenzungsgeometrie der Füllung des Shapes nicht der Geometrie des Shapes. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Für optimale Ergebnisse liegt der ideale Wertebereich für die Zelle **"SketchFillChange"** zwischen 15 % und 50 %. Ein Wert unter 15 % ist wahrnehmbar. Ein Wert, der größer als 50 % ist, wird immer zufälliger. 
  
Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "SketchFillChange"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchFillChange  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle **"SketchFillChange"** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchFillChange** <br/> |
   

