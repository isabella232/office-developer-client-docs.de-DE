---
title: SBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SBinary
api_type:
- COM
ms.assetid: f21b5e6c-7a63-46bf-acbf-0e042e3519f7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: fe07ed7c7f9c76f82b54732c019b9b5f8beb5db2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795422"
---
# <a name="sbinary"></a>SBinary

  
  
**Betrifft**: Outlook 
  
Beschreibt eine Eigenschaft vom Typ PT_BINARY.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SBinary
{
  ULONG      cb;
  LPBYTE     lpb;
} SBinary, FAR *LPSBinary;

```

## <a name="members"></a>Members

 **cb**
  
> Anzahl der Bytes im **Lpb** -Member. 
    
 **lpb**
  
> Zeiger auf den Wert der PT_BINARY-Eigenschaft.
    
## <a name="remarks"></a>Hinweise

Informationen zu Eigenschaftstypen finden Sie unter [MAPI-Eigenschaft Type Overview](mapi-property-type-overview.md).
  
## <a name="see-also"></a>Siehe auch



[SPropValue](spropvalue.md)


[MAPI-Strukturen](mapi-structures.md)

