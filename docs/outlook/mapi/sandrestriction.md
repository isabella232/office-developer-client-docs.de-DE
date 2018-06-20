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
ms.openlocfilehash: 1437130caecd57344fc171d234c5391ea92e1d4b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795435"
---
# <a name="sandrestriction"></a>SAndRestriction

  
  
**Betrifft**: Outlook 
  
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

## <a name="members"></a>Members

 **cRes**
  
> Anzahl der Suche Einschränkungen im Array auf das Element **LpRes** zeigt. 
    
 **lpRes**
  
> Zeiger auf ein Array von [SRestriction](srestriction.md) -Strukturen, die mit **eine Operation** kombiniert werden. 
    
## <a name="remarks"></a>Hinweise

Das Ergebnis der **SAndRestriction** ist TRUE, wenn alle seine untergeordneten Einschränkungen zu TRUE ausgewertet werden. Es ist FALSE, wenn alle untergeordneten Beschränkung auf "false" ausgewertet wird. 
  
Eine Beschreibung der Einschränkungstypen zum Erstellen, und Beispielcode finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

