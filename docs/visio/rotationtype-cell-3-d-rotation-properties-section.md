---
title: RotationType Cell (3-D Rotation Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Bestimmt, ob das Shape eine parallele Drehung, eine Perspektive Drehung oder eine oblique Rotation, als eine ganze Zahl zwischen 0 und 6 folgt.
ms.openlocfilehash: 85effcef3969d7b7c57551ec88710ba84b3fc163
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797909"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>RotationType Cell (3-D Rotation Properties Section)

Bestimmt, ob das Shape eine parallele Drehung, eine Perspektive Drehung oder eine oblique Rotation, als eine ganze Zahl zwischen 0 und 6 folgt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Das Shape hat keine Drehung.  <br/> |
|1  <br/> |Die Form ist eine parallele Drehung.  <br/> |
|2  <br/> |Die Form ist eine Perspektive Drehung.  <br/> |
|3  <br/> |Die Form ist eine obere linke oblique Drehung.  <br/> |
|4  <br/> |Die Form ist eine rechts oblique Top Drehung.  <br/> |
|5  <br/> |Die Form ist eine unteren linken oblique Drehung.  <br/> |
|6  <br/> |Die Form ist eine unten rechts oblique Drehung.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn Sie einen Verweis auf die Zelle **RotationType** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |RotationType  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **RotationType** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRow3DRotationProperties** <br/> |
|Zellenindex:  <br/> |**visRotationType** <br/> |
   

