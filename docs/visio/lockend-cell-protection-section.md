---
title: Zelle "LockEnd" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
ms.localizationpriority: medium
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: Sperrt den Endpunkt (EndeX, EndeY) eines 1D-Shapes an einer bestimmten Position.
ms.openlocfilehash: 35831023adb58b75be973bd6e54c5985eae01c0c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603613"
---
# <a name="lockend-cell-protection-section"></a>Zelle "LockEnd" (Abschnitt "Protection")

Sperrt den Endpunkt (EndeX, EndeY) eines 1D-Shapes an einer bestimmten Position.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Endpunkt ist gesperrt.  <br/> |
| FALSE  <br/> | Endpunkt ist nicht gesperrt.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Um einen Verweis auf die Zelle LockEnd anhand des Namens einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockEnd  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockEnd anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockEnd** <br/> |
   

