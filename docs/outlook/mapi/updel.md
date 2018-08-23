---
title: UPDEL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3b23291d-3355-d772-4647-d4bbd64b0b53
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 057a1ff38ed3809ce03bce8f820f1d16eea7fb46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581125"
---
# <a name="updel"></a><span data-ttu-id="4e464-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="4e464-103">UPDEL</span></span>

  
  
<span data-ttu-id="4e464-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e464-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e464-105">Informationen für Elemente, die in einem lokalen Speicher gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="4e464-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="4e464-106">Diese Informationen werden während der [Upload löschen Status Zustand](upload-delete-status-state.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e464-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4e464-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4e464-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="4e464-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="4e464-108">Members</span></span>

 <span data-ttu-id="4e464-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="4e464-109">_pupde_</span></span>
  
>  <span data-ttu-id="4e464-110">[out] Vektor [UPDELE](updele.md) Einträge.</span><span class="sxs-lookup"><span data-stu-id="4e464-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="4e464-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="4e464-111">_cEnt_</span></span>
  
> <span data-ttu-id="4e464-112">[out] Anzahl der Einträge in *Pupde* .</span><span class="sxs-lookup"><span data-stu-id="4e464-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="4e464-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4e464-113">See also</span></span>



[<span data-ttu-id="4e464-114">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="4e464-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4e464-115">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="4e464-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4e464-116">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4e464-116">MAPI Constants</span></span>](mapi-constants.md)

