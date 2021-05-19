---
title: Zelle "SketchLineChange" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Bestimmt den Umfang der Randomisierung der Linie der Form aus der Geometrie des Shapes, wenn ein Skizzierungseffekt als Prozentsatz der Länge eines Abschnitts verwendet wird. Wenn der Wert der Zelle SketchLineChange auf 0 % festgelegt ist, entspricht die Geometrie der Linie des Shapes der Geometrie des Shapes. Wenn der Wert 100 % beträgt, folgt die Geometrie der Linie des Shapes nicht der Geometrie der Form.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419506"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>Zelle "SketchLineChange" (Abschnitt "Additional Effect Properties")

Bestimmt den Umfang der Randomisierung der Linie der Form aus der Geometrie des Shapes, wenn ein Skizzierungseffekt als Prozentsatz der Länge eines Abschnitts verwendet wird. Wenn der Wert der **Zelle SketchLineChange** auf 0 % festgelegt ist, entspricht die Geometrie der Linie des Shapes der Geometrie des Shapes. Wenn der Wert 100 % beträgt, folgt die Geometrie der Linie des Shapes nicht der Geometrie der Form. 
  
## <a name="remarks"></a>Hinweise

Für optimale Ergebnisse liegt der ideale Wertebereich für die **Zelle SketchLineChange** zwischen 15 % und 50 %. Ein Wert unter 15 % ist kaum wahrnehmbar. Bei einem Wert von mehr als 50 % könnte die Zeile zu viel zufällig gewählt werden. 
  
Verwenden Sie zum Erhalten eines Verweises auf die **Zelle SketchLineChange** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchLineChange  <br/> |
   
Um einen Verweis auf die **Zelle SketchLineChange nach** Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchLineChange** <br/> |
   

