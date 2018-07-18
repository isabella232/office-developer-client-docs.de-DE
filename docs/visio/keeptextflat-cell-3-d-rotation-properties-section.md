---
title: KeepTextFlat Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3537de44-8d6f-4bd9-bf8c-fa851fc007b9
description: Gibt an, ob ein Shape-Text des Shapes Drehung in 3D ignoriert. Gilt nicht für 2D-Diagramme Drehung.
ms.openlocfilehash: cf8b964360e602b81a2a7b7ca79961921eeeb8b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797267"
---
# <a name="keeptextflat-cell-3-d-rotation-properties-section"></a>KeepTextFlat Cell (3-D Rotation Properties Section)

Gibt an, ob ein Shape-Text des Shapes Drehung in 3D ignoriert. Gilt nicht für 2D-Diagramme Drehung. 
  
****

|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Shape-Text wird nicht mit der Shape-Geometrie gedreht.  <br/> |
|FALSE  <br/> |Shape-Text wird so gedreht mit der Shape-Geometrie umgewandelt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **KeepTextFlat** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |KeepTextFlat  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **KeepTextFlat** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRow3DRotationProperties** <br/> |
|Zellenindex:  <br/> |**visKeepTextFlat** <br/> |
   

