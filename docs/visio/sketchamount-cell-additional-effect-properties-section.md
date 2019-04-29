---
title: SketchAmount Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Bestimmt die Verzerrung für einen skizzeneffekt als ganze Zahl zwischen 0 und 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404421"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>SketchAmount Cell (Additional Effect Properties section)

Bestimmt die Verzerrung für einen skizzeneffekt als ganze Zahl zwischen 0 und 25. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Auf die Form wurde kein skizzeneffekt angewendet.  <br/> |
|1-25  <br/> |Die Form hat eine Skizzen Verzerrung, die auf Sie angewendet wurde, wobei der Wert 1 die meisten Verzerrungen und 25 die geringste ist.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **SketchAmount** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchAmount  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchAmount** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchAmount** <br/> |
   

