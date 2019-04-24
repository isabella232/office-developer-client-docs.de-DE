---
title: SketchFillChange Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Bestimmt die Menge der Zufallsgenerierung der Formfüllung aus der Geometrie der Form bei Verwendung eines Skizzen Effekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle SketchFillChange auf 0% festgelegt ist, entspricht die umschließende Geometrie der Füllung einer Form der Geometrie der Form. Wenn der Wert 100% ist, folgt die begrenzungsgeometrie der Füllung der Form nicht der Geometrie der Form.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339812"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a>SketchFillChange Cell (Additional Effect Properties section)

Bestimmt die Menge der Zufallsgenerierung der Formfüllung aus der Geometrie der Form bei Verwendung eines Skizzen Effekts als Prozentsatz der Länge eines Abschnitts. Wenn der Wert der Zelle **SketchFillChange** auf 0% festgelegt ist, entspricht die umschließende Geometrie der Füllung einer Form der Geometrie der Form. Wenn der Wert 100% ist, folgt die begrenzungsgeometrie der Füllung der Form nicht der Geometrie der Form. 
  
## <a name="remarks"></a>Bemerkungen

Optimale Ergebnisse erzielen Sie, wenn der optimale Wert für die **SketchFillChange** -Zelle zwischen 15% und 50% liegt. Ein Wert unter 15% ist kaum spürbar; ein Wert größer als 50% wird zunehmend randomisiert. 
  
Wenn Sie einen Verweis auf die Zelle **SketchFillChange** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchFillChange  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchFillChange** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchFillChange** <br/> |
   

