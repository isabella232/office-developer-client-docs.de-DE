---
title: Zelle "LockVtxEdit" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
localization_priority: Normal
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Sperrt die Scheitelpunkte eines Shapes, sodass sie nicht bearbeitet werden können.
ms.openlocfilehash: 1703769fe54171a14f7052f0f6686e1eb5ec92fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417666"
---
# <a name="lockvtxedit-cell-protection-section"></a>Zelle "LockVtxEdit" (Abschnitt "Protection")

Sperrt die Scheitelpunkte eines Shapes, sodass sie nicht bearbeitet werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Scheitelpunkte können nicht bearbeitet werden.  <br/> |
|FALSE  <br/> |Scheitelpunkte können bearbeitet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Um einen Verweis auf die Zelle LockVtxEdit anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockVtxEdit  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die LockVtxEdit-Zelle nach Index aus einem Programm zu erhalten: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockVtxEdit** <br/> |
   

