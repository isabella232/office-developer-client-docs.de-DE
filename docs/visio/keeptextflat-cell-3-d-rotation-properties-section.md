---
title: KeepTextFlat Cell (3-D Rotation Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Gibt an, ob der Text der Form die Drehung in 3D ignoriert. Gilt nicht für 2D-Rotation.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360438"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>KeepTextFlat Cell (3-D Rotation Properties section)

Gibt an, ob der Text der Form die Drehung in 3D ignoriert. Gilt nicht für 2D-Rotation. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Shape-Text wird nicht mit der Geometrie des Shapes gedreht.  <br/> |
|FALSE  <br/> |Der Shape-Text wird so transformiert, dass er mit der Geometrie des Shapes rotiert.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **KeepTextFlat** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |KeepTextFlat  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **KeepTextFlat** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRow3DRotationProperties** <br/> |
|Zellenindex:  <br/> |**visKeepTextFlat** <br/> |
   

