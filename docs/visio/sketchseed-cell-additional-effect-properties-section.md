---
title: SketchSeed Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Stellt einen zufällige Wert verwendet, um die Geometrie einer Skizze Auswirkung, wie eine positive ganze Zahl zu bestimmen. Der Wert der Zelle SketchSeed wird nach dem Zufallsprinzip erstellt, wenn eine Skizze Auswirkung auf die Form angewendet wird.
ms.openlocfilehash: 7c9d23e19da1a94bb37f1fc916e2f08095976d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798131"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>SketchSeed Cell (Additional Effect Properties Section)

Stellt einen zufällige Wert verwendet, um die Geometrie einer Skizze Auswirkung, wie eine positive ganze Zahl zu bestimmen. Der Wert der Zelle **SketchSeed** wird nach dem Zufallsprinzip erstellt, wenn eine Skizze Auswirkung auf die Form angewendet wird. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **SketchSeed** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchSeed  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchSeed** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchSeed** <br/> |
   

