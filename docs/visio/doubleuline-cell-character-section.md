---
title: Zelle "DoubleULine" (Abschnitt "Character")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm260
localization_priority: Normal
ms.assetid: c18955c8-d653-c29d-d3da-9d3cd0241e17
description: Legt fest, ob der Textbereich doppelt unterstrichen ist.
ms.openlocfilehash: 2708e7f55e1fd04d5fb902b3d382035790cbbcc2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357463"
---
# <a name="doubleuline-cell-character-section"></a>Zelle "DoubleULine" (Abschnitt "Character")

Legt fest, ob der Textbereich doppelt unterstrichen ist.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Text ist doppelt unterstrichen.  <br/> |
|FALSE  <br/> |Text ist nicht doppelt unterstrichen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die Zelle DoubleULine enthält Formatierungsinformationen für einen Unterbereich des Texts eines Shapes, wenn der Abschnitt Character mehrere Zeilen enthält. Andernfalls enthält diese Zelle Formatierungsinformationen für den gesamten Text des Shapes.
  
Sie können den Wert dieser Zelle auch festlegen, indem Sie das Dialogfeld **Text** verwenden (klicken Sie dazu auf der Registerkarte **Start** auf den Pfeil neben **Schriftart**). 
  
Wenn Sie einen Verweis auf die Zelle "DoubleULine aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |Char. DoubleULine [ *i* ] wobei *i* = <1>, 2, 3...  <br/> |
   
Wenn Sie einen Verweis auf die Zelle "DoubleULine aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionCharacter** <br/> |
|Zeilenindex:  <br/> |**visRowCharacter** +  *i* , wobei *i* = 0, 1, 2...  <br/> |
|Zellenindex:  <br/> |**visCharacterDblUnderline** <br/> |
   

