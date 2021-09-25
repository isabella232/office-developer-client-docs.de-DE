---
title: SNotRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SNotRestriction
api_type:
- COM
ms.assetid: e86ca032-d973-4b79-976e-5240ab38a0da
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e49b721bc50465c2b0e3191cc8a57d353fceeb17
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566584"
---
# <a name="snotrestriction"></a>SNotRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine **NOT-Einschränkung,** die verwendet wird, um einen logischen **NOT-Vorgang** auf eine Einschränkung anzuwenden. 
  
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
  
> Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Einschränkung beschreibt, die mit dem logischen **NOT-Operator** verknüpft werden soll. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zur **SNotRestriction-Struktur** finden Sie unter ["Einschränkungen".](about-restrictions.md) 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

