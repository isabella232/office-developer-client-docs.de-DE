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
ms.openlocfilehash: 07a1a0a1953d136da534fbdc6339d326c877bebf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344541"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine **nicht** -Einschränkung, die verwendet wird, um eine logische **Not** -Operation auf eine Einschränkung anzuwenden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
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
  
> Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Einschränkung beschreibt, die dem logischen **Not** -Operator hinzugefügt werden soll. 
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zur **SNotRestriction** -Struktur finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

