---
title: SSubRestriction
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.SSubRestriction
api_type:
- COM
ms.assetid: 5f7012f7-060d-4f2d-bcff-2aa9f6980e71
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8f727951410b7c64b32fc0204989c1204b0dce1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566402"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Unterobjekteinschränkung, die zum Filtern der Zeilen der Anlage- oder Empfängertabelle einer Nachricht verwendet wird.
  
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

## <a name="members"></a>Members

 **ulSubObject**
  
> Typ des Unterobjekts, das als Ziel für die Einschränkung dienen soll. Mögliche Werte sind: 
    
PR_MESSAGE_RECIPIENTS 
  
> Wenden Sie die Einschränkung auf die Empfängertabelle einer Nachricht an. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Wenden Sie die Einschränkung auf die Anlagentabelle einer Nachricht an. 
    
 **lpRes**
  
> Zeiger auf eine [SRestriction-Struktur.](srestriction.md) 
    
## <a name="remarks"></a>HinwBemerkungeneise

Unterobjekteinschränkungen werden nicht von allen Tabellen unterstützt. In der Regel werden nur Ordnerinhaltstabellen und Suchergebnisordner unterstützt. Beispielsweise werden Unterobjekteinschränkungen verwendet, um eine Nachricht zu finden, die einen bestimmten Typ von Anlage oder Empfänger aufweist. 
  
Wenn eine Implementierung keine Unterobjekteinschränkungen unterstützt, wird MAPI_E_TOO_COMPLEX aus den [IMAPITable::Restrict-](imapitable-restrict.md) oder [IMAPITable::FindRow-Methoden](imapitable-findrow.md) zurückgegeben. 
  
Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter ["Einschränkungen".](about-restrictions.md) 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

