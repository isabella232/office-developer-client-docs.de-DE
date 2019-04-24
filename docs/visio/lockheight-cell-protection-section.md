---
title: Zelle "LockHeight" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Sperrt die Höhe des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.
ms.openlocfilehash: 099f6597656d4389476818253f34e741ddd404de
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341776"
---
# <a name="lockheight-cell-protection-section"></a>Zelle "LockHeight" (Abschnitt "Protection")

Sperrt die Höhe des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Höhe ist gesperrt.  <br/> |
| FALSE  <br/> | Höhe ist nicht gesperrt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle LockHeight aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LockHeight  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LockHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockHeight** <br/> |
   

