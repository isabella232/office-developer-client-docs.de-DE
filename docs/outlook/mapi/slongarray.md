---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9b1c5a09a60240efa9d4fa117f0d8fe8113169d5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414529"
---
# <a name="slongarray"></a>SLongArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von LONG-Werttypen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_LONG verwendet werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Die Anzahl der Werte im Array, auf die durch das **LPL** -Element verwiesen wird. 
    
 **LPL**
  
> Zeiger auf ein Array von LONG-Werten.
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu PT_MV_LONG finden Sie unter [Liste der Eigenschaftstypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

