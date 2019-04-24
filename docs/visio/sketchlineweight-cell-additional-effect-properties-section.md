---
title: SketchLineWeight Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Bestimmt die zusätzliche Dicke, die der Linienstärke als Ergebnis eines Skizzen Effekts in Punkt zwischen 0 und 50 hinzugefügt wurde. Die Stärke der Linien einer Form nimmt zu, wenn sich der Wert der SketchLineWeight-Zelle erhöht.
ms.openlocfilehash: 0ee71bbaec59f5c79b72314b08478f8028b4e0ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315120"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a>SketchLineWeight Cell (Additional Effect Properties section)

Bestimmt die zusätzliche Dicke, die der Linienstärke als Ergebnis eines Skizzen Effekts in Punkt zwischen 0 und 50 hinzugefügt wurde. Die Stärke der Linien einer Form nimmt zu, wenn sich der Wert der **SketchLineWeight** -Zelle erhöht. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **SketchLineWeight** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchLineWeight  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchLineWeight** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchLineWeight** <br/> |
   

