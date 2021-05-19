---
title: SLargeIntegerArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SLargeIntegerArray
api_type:
- COM
ms.assetid: 9ec9a674-c1a2-4137-856f-6cabe6f0eb9f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ab82fff2645a5e1861523eb3f1866e0ddc7d13a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331388"
---
# <a name="slargeintegerarray"></a>SLargeIntegerArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array [von LARGE_INTEGER](https://go.microsoft.com/fwlink/?LinkId=132130) Strukturen, die zum Beschreiben einer Eigenschaft vom Typ PT_MV_I8. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLargeIntegerArray
{
  ULONG cValues;
  LARGE_INTEGER FAR *lpli;
} SLargeIntegerArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array, auf das das **lpli-Element verweist.** 
    
 **lpli**
  
> Zeiger auf ein Array von **LARGE_INTEGER,** das die ganzzahligen Werte enthält. 
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zu PT_MV_18 finden Sie [unter List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

