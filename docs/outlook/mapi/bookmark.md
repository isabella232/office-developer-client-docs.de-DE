---
title: Lesezeichen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8f5f3bc454e18b1dbab434fc1b7cc094b0d6a360
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791529"
---
# <a name="bookmark"></a>Lesezeichen

  
  
**Betrifft**: Outlook 
  
Definiert die Textmarken Daten zum Erinnern an einer Position in einer Tabelle. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Zusammenhängenden Methoden:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>Hinweise

MAPI sind drei Textmarken, wie folgt definiert:
  
BOOKMARK_BEGINNING 
  
> Speichert die Anfangsposition der Tabelle an. 
    
BOOKMARK_CURRENT 
  
> Speichert die aktuelle Position in der Tabelle.
    
BOOKMARK_END 
  
> Speichert die Endposition der Tabelle an.
    
Clients können weitere Textmarken zum Erinnern an andere Positionen Tabelle erstellen. Textmarken sind nur ab, wenn die Tabelle geöffnet ist ungültig. Clients müssen Textmarken frei, die sie vor dem Schließen der verknüpften Tabelle erstellt haben. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[MAPI-Datentypen](mapi-data-types.md)

