---
title: SWStringArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SWStringArray
api_type:
- COM
ms.assetid: c1ae24ad-1bbb-4dee-b414-b5226593b6fa
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 68a90d4bcc0b52cfa312fcaa60add644ea835ce0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609487"
---
# <a name="swstringarray"></a>SWStringArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeichenfolgen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_UNICODE zu beschreiben. 
  
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Zeichenfolgen im Array, auf die vom **lppszW-Element** verwiesen wird. 
    
 **lppszW**
  
> Zeiger auf ein Array von Unicode-Zeichenfolgen mit Nullende.
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_UNICODE finden Sie unter [Eigenschaftstypen.](property-types.md)
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

