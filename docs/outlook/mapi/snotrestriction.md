---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 174da93e7682246565b12c4fc4ffa6d1a9de065c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575063"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine **keine** Einschränkung, die mit der eine logische **NOT** -Operation, die eine Einschränkung angewendet. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SNotRestriction
{
  ULONG ulReserved;
  LPSRestriction lpRes;
} SNotRestriction;

```

## <a name="members"></a>Elemente

 **ulReserved**
  
> [in] Reserviert. NULL muss sein.
    
 **lpRes**
  
> Zeiger auf eine [SRestriction](srestriction.md) -Struktur, beschreibt die Einschränkung wieder in den logischen Operator **NOT** aufgenommen werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zur Struktur **SNotRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

