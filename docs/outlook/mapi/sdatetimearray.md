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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 9734adff9c9c7526fc8ff46d17ca913752e104b3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795464"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Betrifft**: Outlook 
  
Enthält ein Array von Zeitwerte, mit denen eine Eigenschaft vom Typ PT_MV_SYSTIME beschrieben.
  
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
  
> Anzahl der Werte im Array auf den Member **Lpft** zeigt. 
    
 **lpft**
  
> Zeiger auf ein Array von [FILETIME](filetime.md) -Strukturen, die Zeitwerte enthalten. 
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zu PT_MV_SYSTIME finden Sie unter [Liste der Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

