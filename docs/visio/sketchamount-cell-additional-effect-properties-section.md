---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Bestimmt die Menge des Distortion für einen Effekt Skizze als ganze Zahl zwischen 0 und 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798125"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>SketchAmount Cell (Additional Effect Properties Section)

Bestimmt die Menge des Distortion für einen Effekt Skizze als ganze Zahl zwischen 0 und 25. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Das Shape ist wirkungslos Skizze angewendet wird.  <br/> |
|1-25  <br/> |Die Form angewendet wird, wobei die meisten Distortion, wird ein Wert von 1 und 25 Skizze Distortion hat die geringste.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **SketchAmount** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchAmount  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchAmount** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchAmount** <br/> |
   

