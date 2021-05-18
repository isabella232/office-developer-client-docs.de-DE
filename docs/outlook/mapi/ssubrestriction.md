---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406325"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Unterobjekteinschränkung, die zum Filtern der Zeilen der Anlage oder Empfängertabelle einer Nachricht verwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>Elemente

 **ulSubObject**
  
> Typ des Unterobjekts, das als Ziel für die Einschränkung dienen soll. Mögliche Werte sind: 
    
PR_MESSAGE_RECIPIENTS 
  
> Wenden Sie die Einschränkung auf die Empfängertabelle einer Nachricht an. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Wenden Sie die Einschränkung auf die Anlagentabelle einer Nachricht an. 
    
 **lpRes**
  
> Zeiger auf eine [SRestriction-Struktur.](srestriction.md) 
    
## <a name="remarks"></a>Hinweise

Unterobjekteinschränkungen werden nicht von allen Tabellen unterstützt. In der Regel werden sie nur von Ordnerinhaltstabellen und Suchergebnissen unterstützt. Beispielsweise werden Unterobjekteinschränkungen verwendet, um eine Nachricht mit einem bestimmten Anlagen- oder Empfängertyp zu finden. 
  
Wenn eine Implementierung keine Unterobjekteinschränkungen unterstützt, gibt sie MAPI_E_TOO_COMPLEX [der imAPITable::Restrict-](imapitable-restrict.md) oder [IMAPITable::FindRow-Methoden](imapitable-findrow.md) zurück. 
  
Eine allgemeine Diskussion über die Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

