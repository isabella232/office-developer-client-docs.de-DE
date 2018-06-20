---
title: SketchEnabled Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0baef353-41a1-4071-b5b4-ae342086fe34
description: Bestimmt, ob eine Skizze Auswirkung auf die Form oder nicht, da ein boolescher Wert angezeigt wird.
ms.openlocfilehash: 7428d54eccce1a62d95a78dbc5fc6770fa5f1a77
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798129"
---
# <a name="sketchenabled-cell-additional-effect-properties-section"></a>SketchEnabled Cell (Additional Effect Properties Section)

Bestimmt, ob eine Skizze Auswirkung auf die Form oder nicht, da ein boolescher Wert angezeigt wird. 
  
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **SketchEnabled** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchEnabled  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchEnabled** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchEnabled** <br/> |
   

