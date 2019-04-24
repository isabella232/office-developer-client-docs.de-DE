---
title: Zelle "LockMoveY" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Sperrt die vertikale Position des Shapes, damit es nicht vertikal verschoben werden kann.
ms.openlocfilehash: 6666d47555f8175b4950f95e1fb15abb8b11bfd5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348349"
---
# <a name="lockmovey-cell-protection-section"></a>Zelle "LockMoveY" (Abschnitt "Protection")

Sperrt die vertikale Position des Shapes, damit es nicht vertikal verschoben werden kann.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Vertikale Position ist gesperrt.  <br/> |
| FALSE  <br/> | Vertikale Position ist nicht gesperrt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Verweis auf die Zelle Zelle LockMoveY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | Zelle LockMoveY  <br/> |
   
Wenn Sie einen Verweis auf die Zelle Zelle LockMoveY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**Konstanten visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockMoveY** <br/> |
   

