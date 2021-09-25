---
title: BOOKMARK
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.BOOKMARK
api_type:
- COM
ms.assetid: 678bdc52-3404-48b2-9154-64ce2a941555
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e0d6ee26ee0b4eaa4dfb76355baeb0b756d56bde
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572081"
---
# <a name="bookmark"></a>BOOKMARK

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Definiert Lesezeichendaten zum Speichern einer Position in einer Tabelle. 
  
|||
|:-----|:-----|
|Headerdatei  <br/> |Mapidefs.h  <br/> |
|Verwandte Methoden:  <br/> |[IMAPITable::CreateBookmark](imapitable-createbookmark.md)[IMAPITable::FreeBookmark](imapitable-freebookmark.md) <br/> |
   
```cpp
typedef ULONG_PTR BOOKMARK;
```

## <a name="remarks"></a>HinwBemerkungeneise

MAPI definiert drei Lesezeichen, die wie folgt aufgelistet sind:
  
BOOKMARK_BEGINNING 
  
> Speichert die Anfangsposition der Tabelle. 
    
BOOKMARK_CURRENT 
  
> Speichert die aktuelle Position der Tabelle.
    
BOOKMARK_END 
  
> Speichert die Endposition der Tabelle.
    
Clients können andere Lesezeichen erstellen, um sich andere Tabellenpositionen zu merken. Lesezeichen sind nur gültig, wenn die Tabelle geöffnet ist. Clients müssen alle Lesezeichen freigeben, die sie erstellt haben, bevor sie die zugeordnete Tabelle schließen. 
  
## <a name="see-also"></a>Siehe auch



[IMAPITable::CreateBookmark](imapitable-createbookmark.md)
  
[IMAPITable::FindRow](imapitable-findrow.md)
  
[IMAPITable::FreeBookmark](imapitable-freebookmark.md)
  
[IMAPITable::SeekRow](imapitable-seekrow.md)


[MAPI-Datentypen](mapi-data-types.md)

