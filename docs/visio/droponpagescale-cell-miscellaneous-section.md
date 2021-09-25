---
title: Zelle "DropOnPageScale" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60042
ms.localizationpriority: medium
ms.assetid: 8927f811-7d8e-ed54-9eec-b86a781168dd
ms.openlocfilehash: d8dad81ea4f20bfc78434e2439dfa70932cc7390
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594545"
---
# <a name="droponpagescale-cell-miscellaneous-section"></a>Zelle "DropOnPageScale" (Abschnitt "Miscellaneous")

Enthält den Prozentsatz, um den ein Shape beim Ablegen auf dem Zeichenblatt skaliert wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

In den folgenden zwei Fällen werden Shapes in Visio so skaliert, dass sie entsprechend auf dem Zeichenblatt angezeigt werden:
  
- Beim Ablegen von Shapes ohne Bemaßung auf skalierten Zeichnungen.
    
- Wenn gemessene Formen auf nicht skalierte Zeichnungen abgelegt werden.
    
Der Prozentsatz in der Zelle DropOnPageScale gibt den Faktor an, um den Visio die Form skaliert haben, entweder nach oben ( \> 100) oder nach unten ( \< 100). Sie können diese Zahl beim Berechnen von festgelegten Werten als Faktor verwenden. 
  
Dieser Wert beträgt für Shapes mit Bemaßung auf skalierten Zeichnungen und für Shapes ohne Bemaßung auf nicht skalierten Zeichnungen 100 %. 
  
Verwenden Sie Folgendes, um einen Verweis auf die Zelle "DropOnPageScale" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | DropOnPageScale  <br/> |
   
Um einen Verweis auf die Zelle DropOnPageScale anhand des Indexes aus einem Programm abzurufen, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowMisc** <br/> |
| Zeilenindex:  <br/> |**visObjDropOnPageScale** <br/> |
   

