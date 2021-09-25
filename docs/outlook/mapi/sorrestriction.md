---
title: SOrRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SOrRestriction
api_type:
- COM
ms.assetid: 6fee29ce-9a34-4e0c-bb71-03120c3f1117
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 20d34d3cdb6eb43ef28b829d7d4a987b8525491b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578571"
---
# <a name="sorrestriction"></a>SOrRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine **OR-Einschränkung,** die verwendet wird, um einen logischen **OR-Vorgang** auf eine Einschränkung anzuwenden. 
  
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

 **Cres**
  
> Anzahl der Strukturen im Array, auf die vom **lpRes-Element** verwiesen wird. 
    
 **lpRes**
  
> Zeiger auf die [SRestriction-Struktur,](srestriction.md) die die Einschränkung beschreibt, die mithilfe des logischen **OR-Vorgangs** verknüpft werden soll. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Weitere Informationen zur **SOrRestriction-Struktur** finden Sie unter ["Einschränkungen".](about-restrictions.md) 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

