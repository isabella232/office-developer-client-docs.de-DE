---
title: Zelle "KeepTextFlat" (Abschnitt "3D Rotation Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Gibt an, ob der Text eines Shapes die Drehung des Shapes in 3D ignoriert. Gilt nicht für 2D-Drehung.
ms.openlocfilehash: fc8cf2fac431645876c7f81ed9864cb6c2036169
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422040"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>Zelle "KeepTextFlat" (Abschnitt "3D Rotation Properties")

Gibt an, ob der Text eines Shapes die Drehung des Shapes in 3D ignoriert. Gilt nicht für 2D-Drehung. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Formtext wird nicht mit der Geometrie des Shapes gedreht.  <br/> |
|FALSE  <br/> |Der Formtext wird so transformiert, dass er mit der Geometrie des Shapes gedreht wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle KeepTextFlat** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |KeepTextFlat  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **KeepTextFlat-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRow3DRotationProperties** <br/> |
|Zellenindex:  <br/> |**visKeepTextFlat** <br/> |
   

