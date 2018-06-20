---
title: RotateGradientWithShape Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6aada005-3403-4666-9779-7ccb5b83b74a
description: Bestimmt, ob eine graduelle Füllung mit einem Shape in 2D Drehung, als ein boolescher Wert dreht.
ms.openlocfilehash: d752f870fd08c1a47dfc7ce193b6976a1bdb2a1f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797865"
---
# <a name="rotategradientwithshape-cell-gradient-properties-section"></a>RotateGradientWithShape Cell (Gradient Properties Section)

Bestimmt, ob eine graduelle Füllung mit einem Shape in 2D Drehung, als ein boolescher Wert dreht.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Farbverlauf wird mit der Form gedreht, wenn die Form um die Drehung Pin gedreht wird. "Top" des Farbverlaufs ist parallel zu den Drehpunkt.  <br/> |
|FALSE  <br/> |Der Farbverlauf wird nicht mit der Form gedreht, bei die Form um die Drehung Pin gedreht wird. "Top" des Farbverlaufs ist parallel zum Zeichenbereich.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **RotateGradientWithShape** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | RotateGradientWithShape  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **RotateGradientWithShape** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowGradientProperties** <br/> |
| Zellenindex:  <br/> |**visRotateGradientWithShape** <br/> |
   

