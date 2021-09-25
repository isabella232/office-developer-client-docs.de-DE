---
title: Zelle "RotationType" (Abschnitt "3D Rotation Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a8d5388a-8fd0-4c6e-9633-e1f03c5bef3b
description: Bestimmt, ob die Form einer parallelen Drehung, einer perspektivische Drehung oder einer schrägen Drehung als ganze Zahl von 0 bis 6 folgt.
ms.openlocfilehash: 7e5929b4bc80ae499174c3f7c290de4d6e5666ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573502"
---
# <a name="rotationtype-cell-3-d-rotation-properties-section"></a>Zelle "RotationType" (Abschnitt "3D Rotation Properties")

Bestimmt, ob die Form einer parallelen Drehung, einer perspektivische Drehung oder einer schrägen Drehung als ganze Zahl von 0 bis 6 folgt. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Die Form hat keine Drehung.  <br/> |
|1  <br/> |Die Form hat eine parallele Drehung.  <br/> |
|2  <br/> |Das Shape hat eine perspektivische Drehung.  <br/> |
|3  <br/> |Die Form hat eine drehungsbedrohte obere linke Drehung.  <br/> |
|4   <br/> |Die Form hat eine Drehung oben rechts schräg.  <br/> |
|5  <br/> |Die Form hat eine Drehung unten links schräg.  <br/> |
|6   <br/> |Die Form hat eine schräge Drehung unten rechts.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die **Zelle RotationType** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |RotationType  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle RotationType** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRow3DRotationProperties** <br/> |
|Zellenindex:  <br/> |**visRotationType** <br/> |
   

