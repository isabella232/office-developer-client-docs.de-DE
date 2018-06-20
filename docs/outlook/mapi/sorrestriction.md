---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 06b9b6a046aaa0f16418f75d402cc5be44f845a3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795597"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**Betrifft**: Outlook 
  
Beschreibt eine Einschränkung **oder** die verwendet wird, um eine logische **OR** -Operation, die eine Einschränkung anzuwenden. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>Members

 **cRes**
  
> Anzahl der im Array Strukturen auf der **LpRes** Member zeigt. 
    
 **lpRes**
  
> Zeiger auf die [SRestriction](srestriction.md) -Struktur, beschreibt die Einschränkung mithilfe des logischen Operators **OR** verknüpft werden. 
    
## <a name="remarks"></a>Hinweise

Weitere Informationen zur Struktur **SOrRestriction** finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

