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
ms.openlocfilehash: 0c72164cac8a37d0372ac93f4ed6d3face966ddb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566663"
---
# <a name="isequalmapiuid"></a>IsEqualMAPIUID

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Makro **IsEqualMAPIUID** gibt TRUE zurück, wenn die zwei **MAPIUID** -Strukturen, die dieselbe ID und FALSE enthalten, wenn nicht der Fall ist. 
  
Das Makro **IsEqualMAPIUID** erfordert, dass die Headerdatei Memory.h enthalten sein. 
  
## <a name="see-also"></a>Siehe auch



[MAPIUID](mapiuid.md)


[Makros im Zusammenhang mit Strukturen](macros-related-to-structures.md)

