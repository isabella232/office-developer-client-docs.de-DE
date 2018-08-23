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
ms.openlocfilehash: dc90f15835de35354a271d87a736366a4caf8dd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578780"
---
# <a name="sdatetimearray"></a>SDateTimeArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array auf den Member **Lpft** zeigt. 
    
 **lpft**
  
> Zeiger auf ein Array von [FILETIME](filetime.md) -Strukturen, die Zeitwerte enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_SYSTIME finden Sie unter [Liste der Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[FILETIME](filetime.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

