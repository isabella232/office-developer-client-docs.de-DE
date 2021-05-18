---
title: Zelle "SketchFillChange" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Bestimmt den Umfang der Randomisierung der Füllung der Form aus der Geometrie der Form, wenn ein Skizzierungseffekt als Prozentsatz der Länge eines Abschnitts verwendet wird. Wenn der Wert der Zelle SketchFillChange auf 0 % festgelegt ist, entspricht die umgebende Geometrie der Füllung eines Shapes der Geometrie der Form. Wenn der Wert 100 % beträgt, folgt die umgebende Geometrie der Füllung des Shapes nicht der Geometrie der Form.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408075"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>Zelle "SketchFillChange" (Abschnitt "Additional Effect Properties")

Bestimmt den Umfang der Randomisierung der Füllung der Form aus der Geometrie der Form, wenn ein Skizzierungseffekt als Prozentsatz der Länge eines Abschnitts verwendet wird. Wenn der Wert der **Zelle SketchFillChange** auf 0 % festgelegt ist, entspricht die umgebende Geometrie der Füllung eines Shapes der Geometrie der Form. Wenn der Wert 100 % beträgt, folgt die umgebende Geometrie der Füllung des Shapes nicht der Geometrie der Form. 
  
## <a name="remarks"></a>Hinweise

Für optimale Ergebnisse liegt der ideale Wertebereich für die **Zelle SketchFillChange** zwischen 15 % und 50 %. Ein Wert unter 15 % ist kaum wahrnehmbar. Ein Wert größer als 50 % wird zunehmend randomisiert. 
  
Um einen Verweis auf die **Zelle SketchFillChange** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchFillChange  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle SketchFillChange** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchFillChange** <br/> |
   

