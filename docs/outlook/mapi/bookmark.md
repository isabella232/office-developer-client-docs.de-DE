---
title: BOOKMARK
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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: be41a9916b6b231d5715cf18fe2b0d804434f2ea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594481"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Definiert die Textmarken Daten zum Erinnern an einer Position in einer Tabelle. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Zusammenhängenden Methoden:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md) [IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>HinwBemerkungeneise

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
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[MAPI-Datentypen](mapi-data-types.md)

