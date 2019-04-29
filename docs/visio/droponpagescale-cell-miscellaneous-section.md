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
  
## <a name="remarks"></a>Bemerkungen

In den folgenden zwei Fällen werden Shapes in Visio so skaliert, dass sie entsprechend auf dem Zeichenblatt angezeigt werden:
  
- Beim Ablegen von Shapes ohne Bemaßung auf skalierten Zeichnungen.
    
- Wenn gemessene Formen auf nicht skalierten Zeichnungen abgelegt werden.
    
Der Prozentsatz in der Zelle Zelle DropOnPageScale gibt den Faktor an, mit dem Visio die Form skaliert hat (\>100) oder nach unten\<(100). Sie können diese Zahl beim Berechnen von festgelegten Werten als Faktor verwenden. 
  
Dieser Wert beträgt für Shapes mit Bemaßung auf skalierten Zeichnungen und für Shapes ohne Bemaßung auf nicht skalierten Zeichnungen 100 %. 
  
Wenn Sie einen Verweis auf die Zelle Zelle DropOnPageScale aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle DropOnPageScale  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle DropOnPageScale aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visObjDropOnPageScale** <br/> |
   

