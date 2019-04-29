---
title: ShapeShdwShow Cell (Fill Format section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Bestimmt, ob die Form einen Schatten anzeigt, als ganze Zahl zwischen 0 und 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422117"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>ShapeShdwShow Cell (Fill Format section)

Bestimmt, ob die Form einen Schatten anzeigt, als ganze Zahl zwischen 0 und 2.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Der Schatten wird immer angezeigt, wenn ein Schatten angegeben wird. Die Schatten für unter Formen werden nicht angezeigt.  <br/> |
|1  <br/> |Rendern Sie keinen Schatten, es sei denn, das Shape hat kein übergeordnetes Element. Verwenden Sie subshape-Schatten, wenn Sie gruppiert werden.  <br/> |
|2  <br/> |Wenn ein Schatten angegeben wird, wird immer ein Schatten angezeigt. Die Schatten für unter Formen werden angezeigt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle **ShapeShdwShow** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeShdwShow  <br/> |
   
Wenn Sie einen Verweis auf die Zelle **ShapeShdwShow** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowFill** <br/> |
| Zellenindex:  <br/> |**visFillShdwShow** <br/> |
   

