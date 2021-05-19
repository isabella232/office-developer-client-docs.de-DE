---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3d20a0932de0fb29ea73e56c37e262c0ccd062c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424924"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [GUID-Strukturen,](guid.md) die zum Beschreiben einer Eigenschaft vom Typ PT_MV_CLSID. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SGuidArray
{
  ULONG cValues;
  GUID FAR *lpguid;
} SGuidArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array, auf die das **lpguid-Element** verweist. 
    
 **lpguid**
  
> Zeiger auf ein Array von **GUID-Strukturen,** das die Klassenbezeichnerwerte enthält. 
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zu PT_MV_CLSID finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

