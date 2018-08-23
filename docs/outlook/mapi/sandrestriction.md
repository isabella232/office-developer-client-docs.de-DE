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
ms.openlocfilehash: 9f8da0902ea4c4a862d279ee80ba566c0473c44e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592325"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Einschränkung **und** , die zur Teilnahme an einer Gruppe von Einschränkungen, die mit einer logischen **AND** -Operation verwendet wird. 
  
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
  
> Anzahl der Suche Einschränkungen im Array auf das Element **LpRes** zeigt. 
    
 **lpRes**
  
> Zeiger auf ein Array von [SRestriction](srestriction.md) -Strukturen, die mit **eine Operation** kombiniert werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Das Ergebnis der **SAndRestriction** ist TRUE, wenn alle seine untergeordneten Einschränkungen zu TRUE ausgewertet werden. Es ist FALSE, wenn alle untergeordneten Beschränkung auf "false" ausgewertet wird. 
  
Eine Beschreibung der Einschränkungstypen zum Erstellen, und Beispielcode finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

