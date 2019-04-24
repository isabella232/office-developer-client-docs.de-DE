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
ms.openlocfilehash: 64348347ea930e6a6a80b9a9075299d2e3109eda
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360704"
---
# <a name="syncstate"></a><span data-ttu-id="b83c1-103">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="b83c1-103">SYNCSTATE</span></span>

<span data-ttu-id="b83c1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b83c1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b83c1-105">Diese Struktur definiert die Status für den Replikationsstatus Computer.</span><span class="sxs-lookup"><span data-stu-id="b83c1-105">This structure defines the states for the replication state machine.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b83c1-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b83c1-106">Quick info</span></span>

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

## <a name="see-also"></a><span data-ttu-id="b83c1-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b83c1-107">See also</span></span>

- [<span data-ttu-id="b83c1-108">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="b83c1-108">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="b83c1-109">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="b83c1-109">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="b83c1-110">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b83c1-110">MAPI Constants</span></span>](mapi-constants.md)

