---
title: Zelle "LockVtxEdit" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251224
ms.localizationpriority: medium
ms.assetid: 966cde5c-f04e-7149-3660-720ffa4f7079
description: Sperrt die Scheitelpunkte eines Shapes, sodass sie nicht bearbeitet werden können.
ms.openlocfilehash: ca90a85a327f9f51380957bcdd3fd5c3ff4a6d36
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612470"
---
# <a name="lockvtxedit-cell-protection-section"></a>Zelle "LockVtxEdit" (Abschnitt "Protection")

Sperrt die Scheitelpunkte eines Shapes, sodass sie nicht bearbeitet werden können.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|TRUE  <br/> |Scheitelpunkte können nicht bearbeitet werden.  <br/> |
|FALSE  <br/> |Scheitelpunkte können bearbeitet werden.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Um einen Verweis auf die Zelle LockVtxEdit anhand des Namens aus einer anderen Formel oder eines Programms mithilfe der **CellsU-Eigenschaft** abzurufen, verwenden Sie Folgendes: 
  
|||
|:-----|:-----|
|Zellenname:  <br/> |LockVtxEdit  <br/> |
   
Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockVtxEdit anhand des Indexes eines Programms abzurufen: 
  
|||
|:-----|:-----|
|Abschnittsindex:  <br/> |**visSectionObject** <br/> |
|Zeilenindex:  <br/> |**visRowLock** <br/> |
|Zellenindex:  <br/> |**visLockVtxEdit** <br/> |
   

