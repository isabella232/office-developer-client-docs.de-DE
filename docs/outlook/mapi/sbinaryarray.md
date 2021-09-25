---
title: SBinaryArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SBinaryArray
api_type:
- COM
ms.assetid: 2d5b7302-cad2-4522-beb1-7c6c711f42e6
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 865cfe1df39c3c4070ac24ba2e2b9ff5aea75a66
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609530"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Enthält ein Array von binären Werten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinaryArray
{
  ULONG cValues;
  SBinary FAR *lpbin;
} SBinaryArray;

```

## <a name="members"></a>Members

 **cValues**
  
> Anzahl der Werte im Array, auf das vom **Lpbin-Element** verwiesen wird. 
    
 **lpbin**
  
> Zeiger auf ein Array von [SBinary-Strukturen,](sbinary.md) die die binären Werte enthalten. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die **SBinaryArray-Struktur** wird verwendet, um Eigenschaften des Typs PT_MV_BINARY zu beschreiben. 
  
Weitere Informationen zu PT_MV_BINARY finden Sie unter [List of Property Types](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

