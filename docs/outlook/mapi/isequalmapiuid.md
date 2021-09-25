---
title: IsEqualMAPIUID
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.IsEqualMAPIUID
api_type:
- COM
ms.assetid: 85d71b73-0630-4c5d-b0e3-b48d27a300d0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 248d0452b45e8e715b067fc96fcd2ab2a52f7323
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556238"
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
  
> Zeiger auf die erste **MAPIUID-Struktur,** die getestet werden soll. 
    
 _lpuid2_
  
> Zeiger auf die zweite **MAPIUID-Struktur,** die getestet werden soll. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Das **IsEqualMAPIUID-Makro** gibt TRUE zurück, wenn die beiden **MAPIUID-Strukturen** denselben Bezeichner enthalten, und FALSE, wenn dies nicht der Fall ist. 
  
Das **IsEqualMAPIUID-Makro** erfordert, dass die Headerdatei Memory.h eingeschlossen wird. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

