---
title: SKEY
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3f1e8291-6153-c308-94be-ca6745ea86a4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 26b08535d81cb961ed0ace70ea227316b30cd526
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573460"
---
# <a name="skey"></a><span data-ttu-id="ede36-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="ede36-103">SKEY</span></span>

  
  
<span data-ttu-id="ede36-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ede36-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ede36-105">Source-Schlüssel für ein Outlook-Element.</span><span class="sxs-lookup"><span data-stu-id="ede36-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ede36-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ede36-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="ede36-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="ede36-107">Members</span></span>

 <span data-ttu-id="ede36-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="ede36-108">_guid_</span></span>
  
> <span data-ttu-id="ede36-109">GUID des Servers, der das Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="ede36-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ede36-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ede36-110">See also</span></span>



[<span data-ttu-id="ede36-111">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="ede36-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ede36-112">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="ede36-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ede36-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="ede36-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="ede36-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="ede36-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="ede36-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="ede36-115">UPREADE</span></span>](upreade.md)

