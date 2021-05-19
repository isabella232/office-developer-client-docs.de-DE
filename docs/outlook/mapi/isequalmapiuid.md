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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 44e3613338c8932bc80dd1150392033dfa3cd050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426933"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Testet zwei [MAPIUID-Strukturen,](mapiuid.md) um festzustellen, ob sie denselben Bezeichner enthalten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Parameter

 _lpuid1_
  
> Zeiger auf die erste **mapIUID-Struktur,** die getestet werden soll. 
    
 _lpuid2_
  
> Zeiger auf die zweite **mapIUID-Struktur,** die getestet werden soll. 
    
## <a name="remarks"></a>Hinweise

Das **IsEqualMAPIUID-Makro** gibt TRUE zurück, wenn die beiden **MAPIUID-Strukturen** denselben Bezeichner und FALSE enthalten, falls nicht. 
  
Das **IsEqualMAPIUID-Makro** erfordert, dass die Headerdatei "Memory.h" enthalten ist. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

