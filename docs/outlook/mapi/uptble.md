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
ms.openlocfilehash: d0b440f01aad7078ed76cd37d36c5ad506215438
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413840"
---
# <a name="uptble"></a><span data-ttu-id="7d752-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="7d752-103">UPTBLE</span></span>

<span data-ttu-id="7d752-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7d752-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7d752-105">Erweiterte Informationen zum Hochladen des Inhalts eines Ordners während des [Status der Uploadtabelle](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="7d752-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7d752-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="7d752-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="7d752-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="7d752-107">Members</span></span>

 <span data-ttu-id="7d752-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="7d752-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="7d752-109">[out] Index, um das Hochladen der  _cEntMod-Anzahl neuer_ oder geänderter Elemente nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="7d752-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="7d752-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="7d752-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="7d752-111">[out] Anzahl der neuen oder geänderten Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="7d752-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="7d752-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="7d752-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="7d752-113">[out] Index zum Nachverfolgen des Hochladens der Anzahl _der cEntRead-Leseelemente._</span><span class="sxs-lookup"><span data-stu-id="7d752-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="7d752-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="7d752-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="7d752-115">[out] Anzahl der Leseelemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="7d752-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="7d752-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="7d752-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="7d752-117">[out] Index zum Nachverfolgen des Hochladens der Anzahl _gelöschter cEntDel-Elemente._</span><span class="sxs-lookup"><span data-stu-id="7d752-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="7d752-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="7d752-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="7d752-119">[out] Die Anzahl der gelöschten Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="7d752-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="7d752-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7d752-120">See also</span></span>

- [<span data-ttu-id="7d752-121">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="7d752-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="7d752-122">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="7d752-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="7d752-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="7d752-123">UPTBL</span></span>](uptbl.md)

