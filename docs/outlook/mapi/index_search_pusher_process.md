---
title: INDEX_SEARCH_PUSHER_PROCESS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6b39504f-6eed-2605-048d-2707f38a7d9a
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ada6d4127d503aae0b068d40d2bb48cb6b833ea0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792682"
---
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="b6e9f-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="b6e9f-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="b6e9f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b6e9f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b6e9f-105">Gibt den Prozess, der an den MAPI-Protokollhandler einer Benachrichtigung sendet, dass ein Objekt in diesen Speicher für die Indizierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="b6e9f-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b6e9f-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b6e9f-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="b6e9f-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="b6e9f-107">Members</span></span>

 <span data-ttu-id="b6e9f-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="b6e9f-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="b6e9f-109">Prozess-ID für den Prozess, der an die Indizierung von der MAPI-Protokollhandler eine Indizierung Benachrichtigung sendet.</span><span class="sxs-lookup"><span data-stu-id="b6e9f-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

