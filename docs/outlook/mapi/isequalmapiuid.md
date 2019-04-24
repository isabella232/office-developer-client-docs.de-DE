---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278736"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Testet zwei [MAPIUID](mapiuid.md) -Strukturen, um zu bestimmen, ob Sie den gleichen Bezeichner enthalten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
|Zugehörige Struktur:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Parameter

 _lpuid1_
  
> Zeiger auf die erste zu testende **MAPIUID** -Struktur. 
    
 _lpuid2_
  
> Zeiger auf die zweite zu testende **MAPIUID** -Struktur. 
    
## <a name="remarks"></a>Bemerkungen

Das **IsEqualMAPIUID** -Makro gibt true zurück, wenn die beiden **MAPIUID** -Strukturen denselben Bezeichner enthalten, und false, wenn dies nicht der Fall ist. 
  
Das **IsEqualMAPIUID** -Makro erfordert, dass die Headerdatei Memory. h enthalten ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

