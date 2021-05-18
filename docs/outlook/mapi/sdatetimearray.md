---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9d9fd04776742383f40c6989bcf588b24b33d84b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406780"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeitwerten, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_SYSTIME.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SDateTimeArray
{
  ULONG cValues;
  FILETIME FAR *lpft;
} SDateTimeArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array, auf die das **lpft-Element verweist.** 
    
 **lpft**
  
> Zeiger auf ein Array von [FILETIME-Strukturen,](filetime.md) die die Zeitwerte enthalten. 
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zu PT_MV_SYSTIME finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

