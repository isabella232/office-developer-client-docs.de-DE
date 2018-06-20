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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a07a7737e9b9354514a2d5ac2ec37a393a3cd4e4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795589"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Betrifft**: Outlook 
  
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

## <a name="members"></a>Members

 **ulReserved**
  
> [in] Reserviert. NULL muss sein.
    
 **lpRes**
  
> Zeiger auf eine [SRestriction](srestriction.md) -Struktur, beschreibt die Einschränkung wieder in den logischen Operator **NOT** aufgenommen werden. 
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zur Struktur **SNotRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

