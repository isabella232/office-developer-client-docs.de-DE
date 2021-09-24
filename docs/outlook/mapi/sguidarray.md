---
title: SGuidArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SGuidArray
api_type:
- COM
ms.assetid: 2091e5fc-75c8-4ea4-87e9-a9bf508e9c58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 156234b52f092c25314603f7f65da2b20bdbbbc5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59550009"
---
# <a name="sguidarray"></a>SGuidArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von [GUID-Strukturen,](guid.md) die verwendet werden, um eine Eigenschaft vom Typ PT_MV_CLSID zu beschreiben. 
  
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array, auf das vom **lpguid-Element** verwiesen wird. 
    
 **lpguid**
  
> Zeiger auf ein Array von **GUID-Strukturen,** die die Klassenbezeichnerwerte enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu PT_MV_CLSID finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[GUID](guid.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

