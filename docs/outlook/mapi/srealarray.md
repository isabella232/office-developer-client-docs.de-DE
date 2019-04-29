---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8439d6609ebece75699a1150a9d0c1a41277fd52
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429873"
---
# <a name="srealarray"></a>SRealArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von float-Werten, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_R4 verwendet werden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Die Anzahl der Werte im Array, auf die durch das **lpflt** -Element verwiesen wird. 
    
 **lpflt**
  
> Zeiger auf ein Array von float-Werten.
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zum PT_MV_R4-Eigenschaftentyp finden Sie unter [Property](property-types.md)Types.
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

