---
title: Zelle RotateGradientWithShape (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Bestimmt, ob ein Füllgradient mit einer Form in 2D-Drehung gedreht wird, als boolescher Wert.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412219"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>Zelle RotateGradientWithShape (Abschnitt "Gradient Properties")

Bestimmt, ob ein Füllgradient mit einer Form in 2D-Drehung gedreht wird, als boolescher Wert.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Farbverlauf dreht sich mit der Form, wenn die Form um den Drehstift gedreht wird. Der "obere Rand" des Farbverlaufs ist parallel zum Drehziehpunkt.  <br/> |
|FALSE  <br/> |Der Farbverlauf dreht sich nicht mit der Form, wenn die Form um den Drehstift gedreht wird. Der "obere Rand" des Farbverlaufs ist parallel zum Zeichenbereich.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle RotateGradientWithShape** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | RotateGradientWithShape  <br/> |
   
Um einen Verweis auf die **RotateGradientWithShape-Zelle** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visRotateGradientWithShape** <br/> |
   

