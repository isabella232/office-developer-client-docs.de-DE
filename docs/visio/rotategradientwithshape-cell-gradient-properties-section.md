---
title: Zelle "RotateGradientWithShape" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Bestimmt, ob ein Füll Verlauf mit einer Form in der 2D-Rotation als boolescher Wert rotiert.
ms.openlocfilehash: 76a76a4a97128c81710269f75e9e17db90827377
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412219"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>Zelle "RotateGradientWithShape" (Abschnitt "Gradient Properties")

Bestimmt, ob ein Füll Verlauf mit einer Form in der 2D-Rotation als boolescher Wert rotiert.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Farbverlauf wird mit der Form gedreht, wenn die Form um die Rotations-Pin gedreht wird. Der "obere" des Farbverlaufs ist parallel zum Drehpunkt.  <br/> |
|FALSE  <br/> |Der Farbverlauf wird nicht mit der Form gedreht, wenn die Form um die Rotations-Pin gedreht wird. Der "obere" des Farbverlaufs ist parallel zum Zeichenbereich.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **RotateGradientWithShape** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | RotateGradientWithShape  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **RotateGradientWithShape** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visRotateGradientWithShape** <br/> |
   

