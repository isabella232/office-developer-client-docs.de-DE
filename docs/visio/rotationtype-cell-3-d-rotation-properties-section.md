---
title: RotationType Cell (3-D Rotation Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Bestimmt, ob die Form einer parallelen Drehung, einer perspektivischen Drehung oder einer schrägen Drehung als ganze Zahl zwischen 0 und 6 folgt.
ms.openlocfilehash: 676f8a15185242aacc1affb9f1bd200ff3df454d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315673"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>RotationType Cell (3-D Rotation Properties section)

Bestimmt, ob die Form einer parallelen Drehung, einer perspektivischen Drehung oder einer schrägen Drehung als ganze Zahl zwischen 0 und 6 folgt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Die Form hat keine Rotation.  <br/> |
|1  <br/> |Die Form hat eine parallele Drehung.  <br/> |
|2  <br/> |Die Form hat eine perspektivische Drehung.  <br/> |
|3  <br/> |Die Form weist eine schräge Drehung oben links auf.  <br/> |
|4  <br/> |Die Form ist oben rechts schräg gedreht.  <br/> |
|5  <br/> |Die Form hat eine schräge linke untere Drehung.  <br/> |
|6  <br/> |Die Form hat eine schräge unten rechts.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die **** Zelle RotationType aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |RotationType  <br/> |
   
Wenn Sie einen Verweis auf die **** Zelle RotationType nach Index aus einem Programm abrufen möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRow3DRotationProperties** <br/> |
|Zellenindex:  <br/> |**visRotationType** <br/> |
   

