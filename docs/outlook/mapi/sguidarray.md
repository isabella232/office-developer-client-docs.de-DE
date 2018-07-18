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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 553ec17e9caf9bf93278ff139eb94e02e6b48554
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19795528"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Betrifft**: Outlook 
  
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
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu PT_MV_CLSID finden Sie unter [Liste der Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

