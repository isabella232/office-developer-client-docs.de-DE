---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 34c7f5f2a17ce4b1fb4ed18bf7c3ab89a18cb658
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556357"
---
# <a name="index_search_pusher_process"></a>INDEX_SEARCH_PUSHER_PROCESS

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Gibt den Prozess an, der eine Benachrichtigung an den MAPI-Protokollhandler sendet, dass ein Objekt in diesem Speicher für die Indizierung bereit ist.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a>Elemente

 *wetterPID* 
  
>  Prozess-ID für den Prozess, der eine Indizierungsbenachrichtigung an den Indexer des MAPI-Protokollhandlers sendet. 
    

