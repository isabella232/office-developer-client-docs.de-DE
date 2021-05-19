---
title: Zelle "SketchSeed" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Stellt einen Randomisierungswert dar, der zum Bestimmen der Geometrie eines Skizziereffekts als positive ganze Zahl verwendet wird. Der Wert der Zelle SketchSeed wird zufällig erstellt, wenn ein Skizziereneffekt auf die Form angewendet wird.
ms.openlocfilehash: 3ec58fbfa183d1a6d7bb6960672658f9a6cca073
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434396"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a>Zelle "SketchSeed" (Abschnitt "Additional Effect Properties")

Stellt einen Randomisierungswert dar, der zum Bestimmen der Geometrie eines Skizziereffekts als positive ganze Zahl verwendet wird. Der Wert der **Zelle SketchSeed** wird zufällig erstellt, wenn ein Skizziereneffekt auf die Form angewendet wird. 
  
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle SketchSeed** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | SketchSeed  <br/> |
   
Um einen Verweis auf die **Zelle SketchSeed nach** Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowOtherEffectProperties** <br/> |
| Zellenindex:  <br/> |**visSketchSeed** <br/> |
   

