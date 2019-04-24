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
ms.openlocfilehash: 9b4ca4628f356142eb5303c064e3916474810fda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345101"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine **oder** -Einschränkung, die zum Anwenden einer logischen **or** -Operation auf eine Einschränkung verwendet wird. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SOrRestriction
{
  ULONG cRes;
  LPSRestriction lpRes;
} SOrRestriction;

```

## <a name="members"></a>Elemente

 **cRes**
  
> Anzahl der Strukturen im Array, auf die durch das **lpRes** -Element verwiesen wird. 
    
 **lpRes**
  
> Zeiger auf die [SRestriction](srestriction.md) -Struktur, die die zu verbindende Einschränkung mit der logischen **or** -Operation beschreibt. 
    
## <a name="remarks"></a>Bemerkungen

Weitere Informationen zur **SOrRestriction** -Struktur finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

