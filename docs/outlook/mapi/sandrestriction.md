---
title: SAndRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SAndRestriction
api_type:
- COM
ms.assetid: 1b7dfe87-f87f-43e3-8332-a0d9c3f70d16
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c31fb0a70dc2458f4db62135d6b371996e2b5dab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59599102"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt  eine AND-Einschränkung, die verwendet wird, um eine Gruppe von Einschränkungen mithilfe eines logischen **AND-Vorgangs** zu verknüpfen. 
  
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

## <a name="members"></a>Members

 **Cres**
  
> Anzahl der Sucheinschränkungen im Array, auf das das **lpRes-Mitglied** verweist. 
    
 **lpRes**
  
> Zeiger auf ein Array von [SRestriction-Strukturen,](srestriction.md) die mit einem logischen **AND-Vorgang** kombiniert werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Ergebnis der **SAndRestriction** ist TRUE, wenn alle untergeordneten Einschränkungen zu TRUE ausgewertet werden. Es ist FALSE, wenn eine untergeordnete Einschränkung als FALSE ausgewertet wird. 
  
Eine Beschreibung der Arten von Einschränkungen, deren Erstellung und Beispielcode finden Sie unter "Informationen zu [Einschränkungen".](about-restrictions.md)
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

