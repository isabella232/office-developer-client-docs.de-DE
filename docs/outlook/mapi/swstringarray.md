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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: ff69981e83d42e439936a3e4be47eabfd811b310
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349553"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeichenfolgen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_UNICODE verwendet werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SWStringArray
{
  ULONG cValues;
  LPWSTR FAR *lppszW;
} SWStringArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Zeichenfolgen im Array, auf die durch das **lppszW** -Element verwiesen wird. 
    
 **lppszW**
  
> Zeiger auf ein Array von Zeichenfolgen mit NULL-Zeichenfolge.
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu PT_MV_UNICODE finden Sie unter [Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

