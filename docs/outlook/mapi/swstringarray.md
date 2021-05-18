---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413605"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeichenzeichenfolgen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_UNICODE. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Zeichenfolgen im Array, auf die das **lppszW-Element** verweist. 
    
 **lppszW**
  
> Zeiger auf ein Array mit Nullend-Unicode-Zeichenzeichenfolgen.
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zu PT_MV_UNICODE finden Sie unter [Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

