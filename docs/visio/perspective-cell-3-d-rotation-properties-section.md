---
title: Perspektivische Zelle (3D-Rotations-Eigenschaften Abschnitt)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e07d97a4-9896-4b88-9e76-5a1b3f133094
description: Bestimmt den Perspektiv Winkel für eine perspektivische Drehung in Grad (0 bis 359,9).
ms.openlocfilehash: 4cbefc2fa147a418fa792542e1dc57c39ab2490c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307770"
---
# <a name="perspective-cell-3-d-rotation-properties-section"></a>Perspektivische Zelle (3D-Rotations-Eigenschaften Abschnitt)

Bestimmt den Perspektiv Winkel für eine perspektivische Drehung in Grad (0 bis 359,9).
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **Perspective** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Perspective  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **Perspective** aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRow3DRotationProperties** <br/> |
|Zellenindex:  <br/> |**visPerspective** <br/> |
   

