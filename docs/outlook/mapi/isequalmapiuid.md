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
ms.openlocfilehash: 635a4a872b83a2996b1a0198975a0ecd2cd906eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792826"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Betrifft**: Outlook 
  
Testet zwei [MAPIUID](mapiuid.md) -Strukturen, um zu bestimmen, ob sie den gleichen Bezeichner enthalten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Struktur:  <br/> |**MAPIUID** <br/> |
   
```cpp
IsEqualMAPIUID(lpuid1, lpuid2)
```

## <a name="parameters"></a>Parameter

 _lpuid1_
  
> Zeiger auf die erste **MAPIUID** Struktur auf getestet werden soll. 
    
 _lpuid2_
  
> Zeiger auf die zweite **MAPIUID** Struktur auf getestet werden soll. 
    
## <a name="remarks"></a>Hinweise

Das Makro **IsEqualMAPIUID** gibt TRUE zurück, wenn die zwei **MAPIUID** -Strukturen, die dieselbe ID und FALSE enthalten, wenn nicht der Fall ist. 
  
Das Makro **IsEqualMAPIUID** erfordert, dass die Headerdatei Memory.h enthalten sein. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

