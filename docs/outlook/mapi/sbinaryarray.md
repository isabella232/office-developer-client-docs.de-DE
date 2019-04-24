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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 12fefbe15491837878608540006e5dd7dc3033ea
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351058"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von binären Werten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Elemente

 **cValues**
  
> Die Anzahl der Werte im Array, auf die durch das **lpbin** -Element verwiesen wird. 
    
 **lpbin**
  
> Zeiger auf ein Array von [SBinary](sbinary.md) -Strukturen, die die Binärwerte enthält. 
    
## <a name="remarks"></a>Bemerkungen

Die **SBinaryArray** -Struktur wird verwendet, um Eigenschaften vom Typ PT_MV_BINARY zu beschreiben. 
  
Weitere Informationen zu PT_MV_BINARY finden Sie unter [Liste der Eigenschaftstypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

