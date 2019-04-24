---
title: SketchEnabled Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0baef353-41a1-4071-b5b4-ae342086fe34
description: Bestimmt, ob ein skizzeneffekt in der Form oder nicht als boolescher Wert angezeigt wird.
ms.openlocfilehash: 713b9b5579ca0503157b9810ebf6ec849651c9c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314784"
---
# <a name="sketchenabled-cell-additional-effect-properties-section"></a>SketchEnabled Cell (Additional Effect Properties section)

Bestimmt, ob ein skizzeneffekt in der Form oder nicht als boolescher Wert angezeigt wird. 
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **SketchEnabled** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchEnabled  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **SketchEnabled** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchEnabled** <br/> |
   

