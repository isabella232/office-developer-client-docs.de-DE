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
ms.openlocfilehash: 8c7ce2805248bf91ce7da071c67ece28a5b8ca07
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564283"
---
# <a name="srealarray"></a>SRealArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Float-Werten, mit denen eine Eigenschaft vom Typ PT_MV_R4 beschrieben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SRealArray
{
  ULONG cValues;
  float FAR *lpflt;
} SRealArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array auf den Member **Lpflt** zeigt. 
    
 **lpflt**
  
> Zeiger auf ein Array von Float-Werten.
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zu den Eigenschaftentyp PT_MV_R4 finden Sie unter [Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

