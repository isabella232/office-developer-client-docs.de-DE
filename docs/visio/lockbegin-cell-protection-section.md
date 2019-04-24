---
title: Zelle "LockBegin" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Sperrt den Anfangspunkt (AnfangX, AnfangY) eines 1D-Shapes an einer bestimmten Position.
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359647"
---
# <a name="lockbegin-cell-protection-section"></a>Zelle "LockBegin" (Abschnitt "Protection")

Sperrt den Anfangspunkt (AnfangX, AnfangY) eines 1D-Shapes an einer bestimmten Position.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Anfangspunkt ist gesperrt.  <br/> |
| FALSE  <br/> | Anfang ist nicht gesperrt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle LockBegin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LockBegin  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LockBegin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockBegin** <br/> |
   

