---
title: UPTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f7fcb385-186d-d5fe-7104-fe0af09d5768
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 62c18ac609547563ad0e98cbd914866e05888ac8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795823"
---
# <a name="uptble"></a><span data-ttu-id="f9b1b-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="f9b1b-103">UPTBLE</span></span>

<span data-ttu-id="f9b1b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9b1b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9b1b-105">Ausführliche Informationen zum Hochladen der Inhalt eines Ordners während der [Tabelle Zustand hochladen](upload-table-state.md)enthält.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="f9b1b-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="f9b1b-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="f9b1b-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="f9b1b-107">Members</span></span>

 <span data-ttu-id="f9b1b-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="f9b1b-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="f9b1b-109">[out] Index zum Nachverfolgen die _cEntMod_ Anzahl der neuen oder geänderten Elemente hochladen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="f9b1b-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="f9b1b-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="f9b1b-111">[out] Anzahl der neuen oder geänderten Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="f9b1b-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="f9b1b-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="f9b1b-113">[out] Indizieren Sie, um nachzuverfolgen, die Anzahl der _cEntRead_ Elemente lesen hochladen.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="f9b1b-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="f9b1b-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="f9b1b-115">[out] Anzahl der gelesenen Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="f9b1b-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="f9b1b-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="f9b1b-117">[out] Index zum Nachverfolgen die Anzahl der _cEntDel_ hochladen gelöschte Elemente.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="f9b1b-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="f9b1b-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="f9b1b-119">[out] Anzahl der gelöschten Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="f9b1b-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f9b1b-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9b1b-120">See also</span></span>

- [<span data-ttu-id="f9b1b-121">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="f9b1b-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="f9b1b-122">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="f9b1b-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="f9b1b-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="f9b1b-123">UPTBL</span></span>](uptbl.md)

