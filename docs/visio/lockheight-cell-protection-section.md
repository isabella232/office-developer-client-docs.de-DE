---
title: Zelle "LockHeight" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
ms.localizationpriority: medium
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Sperrt die Höhe des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.
ms.openlocfilehash: fbc4ef93c7d3df306fe506aa09eed125743912d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582554"
---
# <a name="lockheight-cell-protection-section"></a>Zelle "LockHeight" (Abschnitt "Protection")

Sperrt die Höhe des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Höhe ist gesperrt.  <br/> |
| FALSE  <br/> | Höhe ist nicht gesperrt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle "LockHeight" anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockHeight  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockHeight anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockHeight** <br/> |
   

