---
title: Zelle "LockCalcWH" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm605
ms.localizationpriority: medium
ms.assetid: 6eb51e5a-03d8-3daa-b4e1-6107d540aed9
description: Sperrt das Auswahlrechteck eines Shapes, damit dieses nicht neu berechnet wird, wenn ein Scheitelpunkt bearbeitet oder ein Zeilentyp im Abschnitt Geometry geändert wird.
ms.openlocfilehash: 4d9c6645640c2c53e086cbee384d103421945a72
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603648"
---
# <a name="lockcalcwh-cell-protection-section"></a>Zelle "LockCalcWH" (Abschnitt "Protection")

Sperrt das Auswahlrechteck eines Shapes, damit dieses nicht neu berechnet wird, wenn ein Scheitelpunkt bearbeitet oder ein Zeilentyp im Abschnitt Geometry geändert wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Breite und Höhe können nicht neu berechnet werden.  <br/> |
| FALSE  <br/> | Breite und Höhe können neu berechnet werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Verwenden Sie Folgendes, um einen Verweis auf die Zelle LockCalcWH anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockCalcWH  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockCalcWH anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockCalcWH** <br/> |
   

