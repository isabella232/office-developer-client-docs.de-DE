---
title: SRealArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SRealArray
api_type:
- COM
ms.assetid: 95be07bf-5732-4775-9e0f-fec47e99d9b7
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8c6fc32463fda6589f1cf8b2508c826bbcab1560
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566521"
---
# <a name="srealarray"></a>SRealArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von Float-Werten, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_R4 zu beschreiben. 
  
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

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array, auf das der **lpflt-Member** verweist. 
    
 **lpflt**
  
> Zeiger auf ein Array von Float-Werten.
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zum PT_MV_R4 Eigenschaftentyp finden Sie unter [Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

