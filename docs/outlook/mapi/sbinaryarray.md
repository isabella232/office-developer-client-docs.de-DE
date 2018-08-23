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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e601a59a68a3a7d248165d4e573c5abc34d27e2a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586466"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
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

## <a name="members"></a>Elemente

 **cValues**
  
> Anzahl der Werte im Array auf den Member **Lpbin** zeigt. 
    
 **lpbin**
  
> Zeiger auf ein Array von [SBinary](sbinary.md) -Strukturen, die binäre Werte enthält. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Die Struktur **SBinaryArray** wird verwendet, um Eigenschaften vom Typ PT_MV_BINARY beschreiben. 
  
Weitere Informationen zu PT_MV_BINARY finden Sie unter [Liste der Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

