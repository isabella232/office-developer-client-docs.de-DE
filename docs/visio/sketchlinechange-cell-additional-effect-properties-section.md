---
title: SketchLineChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Bestimmt die Menge der zufällige Zeile aus der Shape-Geometrie des Shapes an, wenn ein Effekt Skizze als Prozentwert der Länge eines Abschnitts mit. Wenn der Wert der Zelle SketchLineChange auf 0 % festgelegt ist, entspricht die Geometrie des Shapes Zeile der Shape-Geometrie. Ist der Wert auf 100 %, folgt die Geometrie Zeile des Shapes nicht die Geometrie des Shapes.
ms.openlocfilehash: 57d2af1a914710d7e5a58686b577014ceb7af424
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798128"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a>SketchLineChange Cell (Additional Effect Properties Section)

Bestimmt die Menge der zufällige Zeile aus der Shape-Geometrie des Shapes an, wenn ein Effekt Skizze als Prozentwert der Länge eines Abschnitts mit. Wenn der Wert der Zelle **SketchLineChange** auf 0 % festgelegt ist, entspricht die Geometrie des Shapes Zeile der Shape-Geometrie. Ist der Wert auf 100 %, folgt die Geometrie Zeile des Shapes nicht die Geometrie des Shapes. 
  
## <a name="remarks"></a>Hinweise

Die besten Ergebnisse zu erzielen ist ideale Wertebereich für die Zelle **SketchLineChange** zwischen 15 % und 50 %. Es wird ein Wert weniger als 15 % kaum Renderingzeit; ein Wert größer als 50 % die Zeile zu viel randomize konnte. 
  
Wenn Sie einen Verweis auf die Zelle **SketchLineChange** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchLineChange  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchLineChange** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchLineChange** <br/> |
   

