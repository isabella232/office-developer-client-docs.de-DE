---
title: Zelle "RotationType" (Abschnitt "3D Rotation Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Bestimmt, ob die Form einer parallelen Drehung, einer Perspektivdrehung oder einer schrägen Drehung als ganze Zahl von 0 bis 6 folgt.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422943"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>Zelle "RotationType" (Abschnitt "3D Rotation Properties")

Bestimmt, ob die Form einer parallelen Drehung, einer Perspektivdrehung oder einer schrägen Drehung als ganze Zahl von 0 bis 6 folgt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Die Form hat keine Drehung.  <br/> |
|1  <br/> |Die Form hat eine parallele Drehung.  <br/> |
|2  <br/> |Die Form hat eine Perspektivdrehung.  <br/> |
|3  <br/> |Die Form hat eine schräge Drehung nach links oben.  <br/> |
|4   <br/> |Die Form hat eine oben rechts schräge Drehung.  <br/> |
|5   <br/> |Die Form hat eine schräge Drehung nach links unten.  <br/> |
|6   <br/> |Die Form hat eine schräge Drehung nach rechts unten.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle RotationType** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |RotationType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **RotationType-Zelle** nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRow3DRotationProperties** <br/> |
|Zellenindex:  <br/> |**visRotationType** <br/> |
   

