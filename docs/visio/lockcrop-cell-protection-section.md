---
title: Zelle "LockCrop" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm610
localization_priority: Normal
ms.assetid: ae05de63-b527-66e6-2c79-056c9c92ec95
description: Sperrt ein Objekt aus einem anderen Programm, damit es nicht mithilfe des Zuschneidetools zugeschnitten werden kann.
ms.openlocfilehash: bfb8bebd50908387fa3f94a8ca228935ef709133
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359626"
---
# <a name="lockcrop-cell-protection-section"></a>Zelle "LockCrop" (Abschnitt "Protection")

Sperrt ein Objekt aus einem anderen Programm, damit es nicht mithilfe des Zuschneidetools zugeschnitten werden kann. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Shape kann nicht zugeschnitten werden.  <br/> |
| FALSE  <br/> | Shape kann zugeschnitten werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle LockCrop aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LockCrop  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LockCrop aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockCrop** <br/> |
   

