---
title: Zelle "ShapeShdwShow" (Abschnitt "Fill Format")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Bestimmt, ob das Shape einen Schatten als ganze Zahl von 0 bis 2 anzeigt.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422117"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a>Zelle "ShapeShdwShow" (Abschnitt "Fill Format")

Bestimmt, ob das Shape einen Schatten als ganze Zahl von 0 bis 2 anzeigt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|0  <br/> |Zeigen Sie den Schatten immer an, wenn ein Schatten angegeben ist. Die Schatten für Unterformen werden nicht angezeigt.  <br/> |
|1  <br/> |Rendern Sie keinen Schatten, es sei denn, die Form verfügt nicht über ein übergeordnetes Element. Verwenden Sie Schatten in Unterform, wenn sie zusammenge gruppieren.  <br/> |
|2  <br/> |Wenn ein Schatten angegeben ist, wird immer ein Schatten angezeigt. Die Schatten für Unterformen werden angezeigt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Verwenden Sie zum Erhalten eines Verweises auf die **Zelle ShapeShdwShow** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:** 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | ShapeShdwShow  <br/> |
   
Um einen Verweis auf die **Zelle ShapeShdwShow** nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowFill** <br/> |
| Zellenindex:  <br/> |**visFillShdwShow** <br/> |
   

