---
title: SketchFillChange Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Bestimmt die Menge der zufälligen Anordnung von der Füllung der Form aus der Shape-Geometrie an, wenn Sie einen Effekt Skizze als Prozentwert der Länge eines Abschnitts verwenden. Wenn der Wert der Zelle SketchFillChange auf 0 % festgelegt ist, entspricht die umgebende Geometrie Füllung einer Form der Shape-Geometrie. Ist der Wert auf 100 %, folgt die umgebende Geometrie der Füllung der Form die Geometrie des Shapes nicht.
ms.openlocfilehash: 8dda34e03188909e167a4abda6f62da3d43c4dd7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798133"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>SketchFillChange Cell (Additional Effect Properties Section)

Bestimmt die Menge der zufälligen Anordnung von der Füllung der Form aus der Shape-Geometrie an, wenn Sie einen Effekt Skizze als Prozentwert der Länge eines Abschnitts verwenden. Wenn der Wert der Zelle **SketchFillChange** auf 0 % festgelegt ist, entspricht die umgebende Geometrie Füllung einer Form der Shape-Geometrie. Ist der Wert auf 100 %, folgt die umgebende Geometrie der Füllung der Form die Geometrie des Shapes nicht. 
  
## <a name="remarks"></a>Hinweise

Die besten Ergebnisse zu erzielen ist ideale Wertebereich für die Zelle **SketchFillChange** zwischen 15 % und 50 %. Es wird ein Wert weniger als 15 % kaum Renderingzeit; ein Wert größer als 50 % ist immer mehr zufällige. 
  
Wenn Sie einen Verweis auf die Zelle **SketchFillChange** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchFillChange  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchFillChange** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchFillChange** <br/> |
   

