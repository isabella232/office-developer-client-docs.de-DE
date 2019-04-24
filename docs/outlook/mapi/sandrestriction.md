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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: da35c9c72f4cf3f076715a7a35a3e3514c672ceb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344660"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine **und-** Einschränkung, die verwendet wird, um einer Gruppe von Einschränkungen mithilfe einer logischen **and-** Operation beizutreten. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SAndRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SAndRestriction;

```

## <a name="members"></a>Elemente

 **cRes**
  
> Die Anzahl der Sucheinschränkungen im Array, auf die durch das **lpRes** -Element verwiesen wird. 
    
 **lpRes**
  
> Zeiger auf ein Array von [SRestriction](srestriction.md) -Strukturen, die mit einer logischen **and-** Operation kombiniert werden. 
    
## <a name="remarks"></a>Bemerkungen

Das Ergebnis des **SAndRestriction** ist true, wenn alle untergeordneten Einschränkungen zu true ausgewertet werden. Er ist FALSE, wenn eine untergeordnete Einschränkung als FALSE ausgewertet wird. 
  
Eine Beschreibung der Einschränkungen, ihre Erstellung und Beispielcode finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

