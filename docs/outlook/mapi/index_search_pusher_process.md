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
ms.openlocfilehash: 64e5cf31dffdc794a22bcbd6d503a2b688f9c733
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423349"
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

 *dwPID* 
  
>  Prozess-ID für den Prozess, der eine Indizierungsbenachrichtigung an den Indexer des MAPI-Protokollhandlers sendet. 
    

