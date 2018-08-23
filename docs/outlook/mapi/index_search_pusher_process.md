---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9495caecd514656f6fd62fb5db6cd8ac2faf4b50
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581741"
---
# <a name="indexsearchpusherprocess"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Gibt den Prozess, der an den MAPI-Protokollhandler einer Benachrichtigung sendet, dass ein Objekt in diesen Speicher für die Indizierung bereit ist.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Elemente

 *dwPID* 
  
>  Prozess-ID für den Prozess, der an die Indizierung von der MAPI-Protokollhandler eine Indizierung Benachrichtigung sendet. 
    

