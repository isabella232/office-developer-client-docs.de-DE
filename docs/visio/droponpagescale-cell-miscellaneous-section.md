---
title: Zelle "DropOnPageScale" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
localization_priority: Normal
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: 17c597df3d9e7e741d902fd566cc9a5de1f31ea0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423762"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>Zelle "DropOnPageScale" (Abschnitt "Miscellaneous")

Enthält den Prozentsatz, um den ein Shape beim Ablegen auf dem Zeichenblatt skaliert wird.
  
## <a name="remarks"></a>Hinweise

In den folgenden zwei Fällen werden Shapes in Visio so skaliert, dass sie entsprechend auf dem Zeichenblatt angezeigt werden:
  
- Beim Ablegen von Shapes ohne Bemaßung auf skalierten Zeichnungen.
    
- Wenn gemessene Formen auf nicht kalibrierte Zeichnungen abgelegt werden.
    
Der Prozentsatz in der Zelle DropOnPageScale gibt den Faktor an, um den Visio die Form skaliert hat, entweder nach oben ( \> 100) oder nach unten ( \< 100). Sie können diese Zahl beim Berechnen von festgelegten Werten als Faktor verwenden. 
  
Dieser Wert beträgt für Shapes mit Bemaßung auf skalierten Zeichnungen und für Shapes ohne Bemaßung auf nicht skalierten Zeichnungen 100 %. 
  
Um einen Verweis auf die Zelle DropOnPageScale anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DropOnPageScale  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DropOnPageScale-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visObjDropOnPageScale** <br/> |
   

