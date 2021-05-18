---
title: Zelle "LockCalcWH" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
localization_priority: Normal
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Sperrt das Auswahlrechteck eines Shapes, damit dieses nicht neu berechnet wird, wenn ein Scheitelpunkt bearbeitet oder ein Zeilentyp im Abschnitt Geometry geändert wird.
ms.openlocfilehash: 2b1d907f480a22a56f5847035da8d1cbde5fdcc5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423041"
---
# <a name="lockcalcwh-cell-protection-section"></a>Zelle "LockCalcWH" (Abschnitt "Protection")

Sperrt das Auswahlrechteck eines Shapes, damit dieses nicht neu berechnet wird, wenn ein Scheitelpunkt bearbeitet oder ein Zeilentyp im Abschnitt Geometry geändert wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Breite und Höhe können nicht neu berechnet werden.  <br/> |
| FALSE  <br/> | Breite und Höhe können neu berechnet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle LockCalcWH anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockCalcWH  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LockCalcWH-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockCalcWH** <br/> |
   

