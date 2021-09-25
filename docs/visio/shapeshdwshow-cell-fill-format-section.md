---
title: Zelle "ShapeShdwShow" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Bestimmt, ob die Form einen Schatten als ganze Zahl von 0 bis 2 anzeigt.
ms.openlocfilehash: 29e7d2a7c900518d933899cedc35a00dcc046e65
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598122"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>Zelle "ShapeShdwShow" (Abschnitt "Fill Format")

Bestimmt, ob die Form einen Schatten als ganze Zahl von 0 bis 2 anzeigt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Zeigt immer den Schatten an, wenn ein Schatten angegeben ist. Die Schatten für Unterformen werden nicht angezeigt.  <br/> |
|1  <br/> |Rendern Sie keinen Schatten, es sei denn, die Form hat kein übergeordnetes Element. Verwenden Sie Unter-Shape-Schatten, wenn sie gruppiert sind.  <br/> |
|2  <br/> |Zeigt immer einen Schatten an, wenn ein Schatten angegeben ist. Die Schatten für Unterformen werden angezeigt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die **Zelle "ShapeShdwShow"** anhand des Namens aus einer anderen Formel, anhand des Werts des **N-Attributs** eines **Cell-Elements** oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeShdwShow  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ShapeShdwShow** anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowFill** <br/> |
| Zellenindex:  <br/> |**visFillShdwShow** <br/> |
   

