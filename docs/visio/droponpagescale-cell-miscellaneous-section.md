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
ms.openlocfilehash: a586cca497e1ba04848142917a84c3aa8a25d081
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796895"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>DropOnPageScale Cell (Miscellaneous Section)

Enthält den Prozentsatz, um den ein Shape beim Ablegen auf dem Zeichenblatt skaliert wird.
  
## <a name="remarks"></a>Hinweise

In den folgenden zwei Fällen werden Shapes in Visio so skaliert, dass sie entsprechend auf dem Zeichenblatt angezeigt werden:
  
- Beim Ablegen von Shapes ohne Bemaßung auf skalierten Zeichnungen.
    
- Wenn die Bemaßung auf nicht skalierten Zeichnungen abgelegt werden.
    
Der Prozentsatz in der Zelle DropOnPageScale gibt den Faktor, mit dem Visio das Shape, entweder nach oben skaliert (\>100) oder nach unten (\<100). Sie können diese Nummer beim Berechnen von hartcodierte Werte als Faktor verwenden. 
  
Dieser Wert beträgt für Shapes mit Bemaßung auf skalierten Zeichnungen und für Shapes ohne Bemaßung auf nicht skalierten Zeichnungen 100 %. 
  
Wenn Sie einen Verweis auf die Zelle DropOnPageScale nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DropOnPageScale  <br/> |
   
Wenn Sie einen Verweis auf die Zelle DropOnPageScale aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zellenindex:  <br/> |**visObjDropOnPageScale** <br/> |
   

