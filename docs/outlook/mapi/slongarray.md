---
title: SLongArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SLongArray
api_type:
- COM
ms.assetid: 57435634-202d-4998-9931-4562f1a66f5f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d1f987f87fb07912115057aed82c0e592e0695c5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619736"
---
# <a name="slongarray"></a>SLongArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von LONG-Werttypen, die verwendet werden, um eine Eigenschaft vom Typ PT_MV_LONG zu beschreiben. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SLongArray
{
  ULONG cValues;
  LONG FAR *lpl;
} SLongArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array, auf das der **lpl-Member** verweist. 
    
 **Lpl**
  
> Zeiger auf ein Array von LONG-Werten.
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zu PT_MV_LONG finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

