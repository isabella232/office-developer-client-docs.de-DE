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
# <a name="indexsearchpusherprocess"></a><span data-ttu-id="db88d-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="db88d-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="db88d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db88d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db88d-105">Gibt den Prozess, der an den MAPI-Protokollhandler einer Benachrichtigung sendet, dass ein Objekt in diesen Speicher für die Indizierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="db88d-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="db88d-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="db88d-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="db88d-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="db88d-107">Members</span></span>

 <span data-ttu-id="db88d-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="db88d-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="db88d-109">Prozess-ID für den Prozess, der an die Indizierung von der MAPI-Protokollhandler eine Indizierung Benachrichtigung sendet.</span><span class="sxs-lookup"><span data-stu-id="db88d-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

