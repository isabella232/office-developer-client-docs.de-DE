---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 468dfd634c4aaf18b019d06975ec9066c9d5f7a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793135"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="2de04-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="2de04-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="2de04-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2de04-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2de04-105">Die MAPIOFFLINE_NOTIFY_TYPE einer Benachrichtigung gibt an, ob eine Änderung in den Verbindungsstatus ist stattfinden soll, erfolgt oder abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2de04-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2de04-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2de04-106">Quick info</span></span>

<span data-ttu-id="2de04-107">Finden Sie unter **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="2de04-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="2de04-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2de04-108">See also</span></span>



[<span data-ttu-id="2de04-109">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="2de04-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="2de04-110">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="2de04-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2de04-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="2de04-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

