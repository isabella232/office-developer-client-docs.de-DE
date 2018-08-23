---
title: MAPIOFFLINE_NOTIFY_TYPE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a111d7b7-6e87-4958-8f9b-0f2adbeb8b63
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: e7120b843eae8df70cb2c4f9cbf581dcf0e09c11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566887"
---
# <a name="mapiofflinenotifytype"></a><span data-ttu-id="faa77-103">MAPIOFFLINE_NOTIFY_TYPE</span><span class="sxs-lookup"><span data-stu-id="faa77-103">MAPIOFFLINE_NOTIFY_TYPE</span></span>

  
  
<span data-ttu-id="faa77-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="faa77-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="faa77-105">Die MAPIOFFLINE_NOTIFY_TYPE einer Benachrichtigung gibt an, ob eine Änderung in den Verbindungsstatus ist stattfinden soll, erfolgt oder abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="faa77-105">The MAPIOFFLINE_NOTIFY_TYPE of a notification identifies if a change in the connection state is going to take place, is taking place, or has completed.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="faa77-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="faa77-106">Quick info</span></span>

<span data-ttu-id="faa77-107">Finden Sie unter **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="faa77-107">See **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
  
```cpp
typedef enum { 
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_START = 1,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE = 2,  
    MAPIOFFLINE_NOTIFY_TYPE_STATECHANGE_DONE = 3  
} MAPIOFFLINE_NOTIFY_TYPE;
```

## <a name="see-also"></a><span data-ttu-id="faa77-108">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="faa77-108">See also</span></span>



[<span data-ttu-id="faa77-109">Informationen zu der Offlinestatus-API</span><span class="sxs-lookup"><span data-stu-id="faa77-109">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="faa77-110">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="faa77-110">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="faa77-111">MAPIOFFLINE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="faa77-111">MAPIOFFLINE_NOTIFY</span></span>](mapioffline_notify.md)

