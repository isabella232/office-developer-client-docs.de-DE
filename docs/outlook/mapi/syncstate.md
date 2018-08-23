---
title: SYNCSTATE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63c47e94-f603-aef9-afed-e3819bd79408
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a27f38e759862c7091205a6f9a8aa1cde90c38e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575532"
---
# <a name="syncstate"></a><span data-ttu-id="09f0a-103">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="09f0a-103">SYNCSTATE</span></span>

<span data-ttu-id="09f0a-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09f0a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09f0a-105">Diese Struktur definiert die Zustände für die Replikation Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="09f0a-105">This structure defines the states for the replication state machine.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="09f0a-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="09f0a-106">Quick info</span></span>

```cpp
typedef enum { 
    LR_SYNC_IDLE = 0, 
    LR_SYNC, 
    LR_SYNC_UPLOAD_HIERARCHY, 
    LR_SYNC_UPLOAD_FOLDER, 
    LR_SYNC_CONTENTS, 
    LR_SYNC_UPLOAD_TABLE, 
    LR_SYNC_UPLOAD_MESSAGE, 
    LR_SYNC_UPLOAD_MESSAGE_READ = 8, 
    LR_SYNC_UPLOAD_MESSAGE_DEL, 
    LR_SYNC_DOWNLOAD_HIERARCHY, 
    LR_SYNC_DOWNLOAD_TABLE, 
    LR_SYNC_DOWNLOAD_HEADER = 17 
} SYNCSTATE; 

```

## <a name="see-also"></a><span data-ttu-id="09f0a-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09f0a-107">See also</span></span>

- [<span data-ttu-id="09f0a-108">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="09f0a-108">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="09f0a-109">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="09f0a-109">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="09f0a-110">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="09f0a-110">MAPI Constants</span></span>](mapi-constants.md)

