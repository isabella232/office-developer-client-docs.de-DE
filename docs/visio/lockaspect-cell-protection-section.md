---
title: Zelle "LockAspect" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Sperrt das Seitenverhältnis des Shapes, sodass die Größe des Shapes nur proportional geändert werden kann. Die Größe kann nicht in einer einzelnen Dimension geändert werden.
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411582"
---
# <a name="lockaspect-cell-protection-section"></a>Zelle "LockAspect" (Abschnitt "Protection")

Sperrt das Seitenverhältnis des Shapes, sodass die Größe des Shapes nur proportional geändert werden kann. Die Größe kann nicht in einer einzelnen Dimension geändert werden.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
| TRUE  <br/> | Seitenverhältnis ist gesperrt.  <br/> |
| FALSE  <br/> | Seitenverhältnis ist nicht gesperrt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle LockAspect anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
| Zellenname:  <br/> | LockAspect  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockAspect nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
| Abschnittsindex:  <br/> |**visSectionObject** <br/> |
| Zeilenindex:  <br/> |**visRowLock** <br/> |
| Zellenindex:  <br/> |**visLockAspect** <br/> |
   

