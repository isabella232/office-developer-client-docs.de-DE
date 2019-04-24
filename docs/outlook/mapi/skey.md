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
ms.openlocfilehash: c417e6f4412bc40e8c2ebc056514eb96f60798f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282677"
---
# <a name="skey"></a><span data-ttu-id="84573-103">SKEY</span><span class="sxs-lookup"><span data-stu-id="84573-103">SKEY</span></span>

  
  
<span data-ttu-id="84573-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84573-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84573-105">Quellschlüssel für ein Outlook-Element.</span><span class="sxs-lookup"><span data-stu-id="84573-105">Source key for an Outlook item.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="84573-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="84573-106">Quick info</span></span>

```cpp
struct SKEY 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
};
```

## <a name="members"></a><span data-ttu-id="84573-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="84573-107">Members</span></span>

 <span data-ttu-id="84573-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="84573-108">_guid_</span></span>
  
> <span data-ttu-id="84573-109">GUID des Servers, der das Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="84573-109">GUID of the server creating the object.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="84573-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84573-110">See also</span></span>



[<span data-ttu-id="84573-111">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="84573-111">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="84573-112">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="84573-112">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="84573-113">UPDELE</span><span class="sxs-lookup"><span data-stu-id="84573-113">UPDELE</span></span>](updele.md)
  
[<span data-ttu-id="84573-114">UPMSG</span><span class="sxs-lookup"><span data-stu-id="84573-114">UPMSG</span></span>](upmsg.md)
  
[<span data-ttu-id="84573-115">UPREADE</span><span class="sxs-lookup"><span data-stu-id="84573-115">UPREADE</span></span>](upreade.md)

