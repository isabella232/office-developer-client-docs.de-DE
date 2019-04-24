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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e176f280cbe15b9c15697b03eb9738887c2924c9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336414"
---
# <a name="ssubrestriction"></a>SSubRestriction

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Beschreibt eine Unterobjekt Einschränkung, die zum Filtern der Zeilen der Anlage-oder Empfängertabelle einer Nachricht verwendet wird.
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs. h  <br/> |
   
```cpp
typedef struct _SSubRestriction
{
  ULONG ulSubObject;
  LPSRestriction lpRes;
} SSubRestriction;

```

## <a name="members"></a>Elemente

 **ulSubObject**
  
> Der Typ des untergeordneten Objekts, das als Ziel für die Einschränkung dienen soll. Folgende Werte sind möglich: 
    
PR_MESSAGE_RECIPIENTS 
  
> Wendet die Einschränkung auf die Empfängertabelle einer Nachricht an. 
    
PR_MESSAGE_ATTACHMENTS 
  
>  Wendet die Einschränkung auf die Anlagentabelle einer Nachricht an. 
    
 **lpRes**
  
> Zeiger auf eine [SRestriction](srestriction.md) -Struktur. 
    
## <a name="remarks"></a>Bemerkungen

Unterobjekt Einschränkungen werden von allen Tabellen nicht unterstützt. In der Regel werden nur Ordnerinhaltstabellen und Suchergebnisordner unterstützt. Unterobjekt Einschränkungen werden beispielsweise verwendet, um Nachrichten zu suchen, die einen bestimmten Anlagen-oder Empfängertyp aufweisen. 
  
Wenn eine Implementierung Unterobjekt Einschränkungen nicht unterstützt, wird MAPI_E_TOO_COMPLEX von den [IMAPITable:: Restrict](imapitable-restrict.md) -oder [IMAPITable:: FindRow](imapitable-findrow.md) -Methoden zurückgegeben. 
  
Eine allgemeine Erläuterung der Funktionsweise von Einschränkungen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md). 
  
## <a name="see-also"></a>Siehe auch



[SRestriction](srestriction.md)


[MAPI-Strukturen](mapi-structures.md)

