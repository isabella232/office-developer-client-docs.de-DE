---
title: SketchSeed Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Stellt einen Zufallswert dar, der verwendet wird, um die Geometrie eines Skizzen Effekts als positive Ganzzahl zu bestimmen. Der Wert der SketchSeed-Zelle wird nach dem Zufallsprinzip erstellt, wenn ein skizzeneffekt auf die Form angewendet wird.
ms.openlocfilehash: 3ec58fbfa183d1a6d7bb6960672658f9a6cca073
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315148"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>SketchSeed Cell (Additional Effect Properties section)

Stellt einen Zufallswert dar, der verwendet wird, um die Geometrie eines Skizzen Effekts als positive Ganzzahl zu bestimmen. Der Wert der **SketchSeed** -Zelle wird nach dem Zufallsprinzip erstellt, wenn ein skizzeneffekt auf die Form angewendet wird. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **SketchSeed** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchSeed  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchSeed** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchSeed** <br/> |
   

