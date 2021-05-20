---
title: Zelle "FillGradientEnabled" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Bestimmt, ob für diese Form ein Füllgradient aktiviert ist.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431211"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a>Zelle "FillGradientEnabled" (Abschnitt "Gradient Properties")

Bestimmt, ob für diese Form ein Füllgradient aktiviert ist. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Die Farbverlaufsfüllung wird auf der Form angezeigt.  <br/> |
|FALSE  <br/> |Farbverlaufsfüllungen werden in der Form nicht angezeigt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die **FillGradientEnabled-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | FillGradientEnabled  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **FillGradientEnabled-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visFillGradientEnabled ** <br/> |
   

