---
title: Zelle "KeepTextFlat" (Abschnitt "3D Rotation Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Gibt an, ob der Text eines Shapes die Drehung des Shapes in 3D ignoriert. Gilt nicht für die 2D-Drehung.
ms.openlocfilehash: a37cfabe00742f7850fd1fa9a1faab7a6be8e5a4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618742"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>Zelle "KeepTextFlat" (Abschnitt "3D Rotation Properties")

Gibt an, ob der Text eines Shapes die Drehung des Shapes in 3D ignoriert. Gilt nicht für die 2D-Drehung. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Der Shape-Text wird nicht mit der Geometrie des Shapes gedreht.  <br/> |
|FALSE  <br/> |Der Shape-Text wird so transformiert, dass er mit der Geometrie des Shapes gedreht wird.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Verwenden Sie Folgendes, um einen Verweis auf die Zelle **"KeepTextFlat"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |KeepTextFlat  <br/> |
   
Um einen Verweis auf die Zelle **KeepTextFlat** anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRow3DRotationProperties** <br/> |
|Zellenindex:  <br/> |**visKeepTextFlat** <br/> |
   

