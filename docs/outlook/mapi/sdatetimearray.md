---
title: SDateTimeArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SDateTimeArray
api_type:
- COM
ms.assetid: 6a0dff65-1055-487c-9d15-4cfe336f2ad7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: af16c7ab02a2cc5dbc72f828d29e292547051d95
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578690"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Zeitwerten, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_SYSTIME zu beschreiben.
  
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array, auf die vom **lpft-Element** verwiesen wird. 
    
 **lpft**
  
> Zeiger auf ein Array von [FILETIME-Strukturen,](filetime.md) die die Zeitwerte enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_SYSTIME finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

