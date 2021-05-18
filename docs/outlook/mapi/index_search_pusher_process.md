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
# <a name="index_search_pusher_process"></a><span data-ttu-id="b5951-103">INDEX_SEARCH_PUSHER_PROCESS</span><span class="sxs-lookup"><span data-stu-id="b5951-103">INDEX_SEARCH_PUSHER_PROCESS</span></span>

  
  
<span data-ttu-id="b5951-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b5951-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b5951-105">Gibt den Prozess an, der eine Benachrichtigung an den MAPI-Protokollhandler sendet, dass ein Objekt in diesem Speicher für die Indizierung bereit ist.</span><span class="sxs-lookup"><span data-stu-id="b5951-105">Specifies the process that is sending a notification to the MAPI Protocol Handler that an object in that store is ready for indexing.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b5951-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b5951-106">Quick info</span></span>

```cpp
typedef struct _INDEX_SEARCH_PUSHER_PROCESS {  
    DWORD dwPID;  
} INDEX_SEARCH_PUSHER_PROCESS; 
```

## <a name="members"></a><span data-ttu-id="b5951-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="b5951-107">Members</span></span>

 <span data-ttu-id="b5951-108">*dwPID*</span><span class="sxs-lookup"><span data-stu-id="b5951-108">*dwPID*</span></span> 
  
>  <span data-ttu-id="b5951-109">Prozess-ID für den Prozess, der eine Indizierungsbenachrichtigung an den Indexer des MAPI-Protokollhandlers sendet.</span><span class="sxs-lookup"><span data-stu-id="b5951-109">Process ID for the process that is sending an indexing notification to the indexer of the MAPI Protocol Handler.</span></span> 
    

