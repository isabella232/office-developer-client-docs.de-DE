---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438883"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine **AND-Einschränkung,** die zum Beitreten zu einer Gruppe von Einschränkungen mithilfe eines logischen **AND-Vorgangs verwendet** wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Elemente

 **cRes**
  
> Anzahl der Sucheinschränkungen im Array, auf die das **lpRes-Element** verweist. 
    
 **lpRes**
  
> Zeiger auf ein Array von [SRestriction-Strukturen,](srestriction.md) das mit einem logischen **AND-Vorgang kombiniert** wird. 
    
## <a name="remarks"></a>Hinweise

Das Ergebnis der **SAndRestriction** ist TRUE, wenn alle untergeordneten Einschränkungen auf TRUE ausgewertet werden. Es ist FALSE, wenn eine untergeordnete Einschränkung auf FALSE ausgewertet wird. 
  
Eine Beschreibung der Arten von Einschränkungen, deren Erstellung und Beispielcode finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

