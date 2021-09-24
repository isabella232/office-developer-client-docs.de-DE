---
title: Zelle "SketchAmount" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Bestimmt die Verzerrung für einen Skizzeneffekt als ganze Zahl zwischen 0 und 25.
ms.openlocfilehash: dc33ea18881cce3d7e5a31f4522074a7b942ddb4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549602"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a>Zelle "SketchAmount" (Abschnitt "Additional Effect Properties")

Bestimmt die Verzerrung für einen Skizzeneffekt als ganze Zahl zwischen 0 und 25. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Auf die Form wird kein Skizzeneffekt angewendet.  <br/> |
|1-25  <br/> |Auf die Form wird eine Skizzenverzerrung angewendet, wobei der Wert 1 die Verzerrung am stärksten und 25 die geringste ist.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "SketchAmount"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchAmount  <br/> |
   
Um einen Verweis auf die **Zelle "SketchAmount"** anhand des Indexes eines Programms abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchAmount** <br/> |
   

