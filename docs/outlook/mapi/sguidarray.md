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
ms.openlocfilehash: bc0ae6d69db6077c17d2efa66d04a5366f2395a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585570"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [GUID](guid.md) -Strukturen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_CLSID beschrieben. 
  
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
  
> Anzahl der Werte im Array auf den Member **x Lpguid** zeigt. 
    
 **x lpguid**
  
> Zeiger auf ein Array von **GUID** -Strukturen, die die Klasse ID-Werte enthält. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_CLSID finden Sie unter [Liste der Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

