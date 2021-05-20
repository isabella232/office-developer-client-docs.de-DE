---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438288"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array mit binären Werten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array, auf die das **lpbin-Element** verweist. 
    
 **lpbin**
  
> Zeiger auf ein Array von [SBinary-Strukturen,](sbinary.md) das die binären Werte enthält. 
    
## <a name="remarks"></a>Hinweise

Die **SBinaryArray-Struktur** wird verwendet, um Eigenschaften vom Typ PT_MV_BINARY. 
  
Weitere Informationen zu PT_MV_BINARY finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

