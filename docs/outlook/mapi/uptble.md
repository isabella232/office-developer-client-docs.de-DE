---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b2523c149d98dacf9ad321a4a443382a39753fd5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592339"
---
# <a name="uptble"></a><span data-ttu-id="fc996-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="fc996-103">UPTBLE</span></span>

<span data-ttu-id="fc996-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc996-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc996-105">Ausführliche Informationen zum Hochladen der Inhalt eines Ordners während der [Tabelle Zustand hochladen](upload-table-state.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="fc996-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="fc996-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="fc996-106">Quick info</span></span>

```cpp
struct UPTBLE 
{ 
    UINTiEntMod; 
    UINTcEntMod; 
    UINTiEntRead; 
    UINTcEntRead; 
    UINTiEntDel; 
    UINTcEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="fc996-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="fc996-107">Members</span></span>

 <span data-ttu-id="fc996-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="fc996-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="fc996-109">[out] Index zum Nachverfolgen die _cEntMod_ Anzahl der neuen oder geänderten Elemente hochladen.</span><span class="sxs-lookup"><span data-stu-id="fc996-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="fc996-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="fc996-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="fc996-111">[out] Anzahl der neuen oder geänderten Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="fc996-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="fc996-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="fc996-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="fc996-113">[out] Indizieren Sie, um nachzuverfolgen, die Anzahl der _cEntRead_ Elemente lesen hochladen.</span><span class="sxs-lookup"><span data-stu-id="fc996-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="fc996-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="fc996-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="fc996-115">[out] Anzahl der gelesenen Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="fc996-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="fc996-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="fc996-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="fc996-117">[out] Index zum Nachverfolgen die Anzahl der _cEntDel_ hochladen gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="fc996-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="fc996-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="fc996-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="fc996-119">[out] Anzahl der gelöschten Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="fc996-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="fc996-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc996-120">See also</span></span>

- [<span data-ttu-id="fc996-121">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="fc996-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="fc996-122">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="fc996-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="fc996-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="fc996-123">UPTBL</span></span>](uptbl.md)

