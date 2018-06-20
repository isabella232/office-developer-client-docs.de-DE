---
title: SYNCHRONISIERUNGSSTATUS
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 63c47e94-f603-aef9-afed-e3819bd79408
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 080556a7ed4530bb96db20fd96d9dda86672a720
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795716"
---
# <a name="syncstate"></a><span data-ttu-id="d68ce-103">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="d68ce-103">SYNCSTATE</span></span>

<span data-ttu-id="d68ce-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d68ce-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d68ce-105">Diese Struktur definiert die Zustände für die Replikation Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="d68ce-105">This structure defines the states for the replication state machine.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d68ce-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="d68ce-106">Quick info</span></span>

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

## <a name="see-also"></a><span data-ttu-id="d68ce-107">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d68ce-107">See also</span></span>

- [<span data-ttu-id="d68ce-108">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="d68ce-108">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="d68ce-109">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="d68ce-109">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="d68ce-110">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="d68ce-110">MAPI Constants</span></span>](mapi-constants.md)

