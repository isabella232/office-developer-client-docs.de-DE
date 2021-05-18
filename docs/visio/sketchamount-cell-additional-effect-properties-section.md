---
title: Zelle "SketchAmount" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Bestimmt den Umfang der Verzerrung für einen Skizziereffekt als ganze Zahl zwischen 0 und 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404421"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>Zelle "SketchAmount" (Abschnitt "Additional Effect Properties")

Bestimmt den Umfang der Verzerrung für einen Skizziereffekt als ganze Zahl zwischen 0 und 25. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Die Form hat keinen Skizzeseffekt, der auf sie angewendet wird.  <br/> |
|1-25  <br/> |Auf die Form wurde eine Zierzeichnung angewendet, wobei der Wert 1 die größte Verzerrung und 25 die geringste Verzerrung ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle SketchAmount** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchAmount  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle SketchAmount** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchAmount** <br/> |
   

