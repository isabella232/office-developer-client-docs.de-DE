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
ms.openlocfilehash: fd9a8d731d141dbb71a204a2d20b268951bef42f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795425"
---
# <a name="sbinaryarray"></a>SBinaryArray

  
  
**Betrifft**: Outlook 
  
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
  
> Anzahl der Werte im Array auf den Member **Lpbin** zeigt. 
    
 **lpbin**
  
> Zeiger auf ein Array von [SBinary](sbinary.md) -Strukturen, die binäre Werte enthält. 
    
## <a name="remarks"></a>Hinweise

Die Struktur **SBinaryArray** wird verwendet, um Eigenschaften vom Typ PT_MV_BINARY beschreiben. 
  
Weitere Informationen zu PT_MV_BINARY finden Sie unter [Liste der Eigenschaftentypen](property-types.md).
  
## <a name="see-also"></a>Siehe auch



[SBinary](sbinary.md)
  
[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

