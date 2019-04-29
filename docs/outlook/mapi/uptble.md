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
# <a name="uptble"></a><span data-ttu-id="488a9-103">UPTBLE</span><span class="sxs-lookup"><span data-stu-id="488a9-103">UPTBLE</span></span>

<span data-ttu-id="488a9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="488a9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="488a9-105">Erweiterte Informationen zum Hochladen der Inhalte eines Ordners während des [Upload-Tabellenstatus](upload-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="488a9-105">Extended information for uploading the contents of a folder during the [upload table state](upload-table-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="488a9-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="488a9-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="488a9-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="488a9-107">Members</span></span>

 <span data-ttu-id="488a9-108">_iEntMod_</span><span class="sxs-lookup"><span data-stu-id="488a9-108">_iEntMod_</span></span>
  
>  <span data-ttu-id="488a9-109">Out Index zum Nachverfolgen des Hochladens der _cEntMod_ Anzahl neuer oder geänderter Elemente.</span><span class="sxs-lookup"><span data-stu-id="488a9-109">[out] Index to track uploading the  _cEntMod_ number of new or modified items.</span></span> 
    
 <span data-ttu-id="488a9-110">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="488a9-110">_cEntMod_</span></span>
  
>  <span data-ttu-id="488a9-111">Out Anzahl der neuen oder geänderten Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="488a9-111">[out] Number of new or modified items in the folder.</span></span> 
    
 <span data-ttu-id="488a9-112">_iEntRead_</span><span class="sxs-lookup"><span data-stu-id="488a9-112">_iEntRead_</span></span>
  
>  <span data-ttu-id="488a9-113">Out Index zum Nachverfolgen des Hochladens der Anzahl von _cEntRead_ -Lese Elementen.</span><span class="sxs-lookup"><span data-stu-id="488a9-113">[out] Index to track uploading the number of  _cEntRead_ read items.</span></span> 
    
 <span data-ttu-id="488a9-114">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="488a9-114">_cEntRead_</span></span>
  
>  <span data-ttu-id="488a9-115">Out Die Anzahl der gelesenen Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="488a9-115">[out] Number of read items in the folder.</span></span> 
    
 <span data-ttu-id="488a9-116">_iEntDel_</span><span class="sxs-lookup"><span data-stu-id="488a9-116">_iEntDel_</span></span>
  
>  <span data-ttu-id="488a9-117">Out Index zum Nachverfolgen des Uploads der Anzahl von _cEntDel_ gelöschten Elementen.</span><span class="sxs-lookup"><span data-stu-id="488a9-117">[out] Index to track uploading the number of  _cEntDel_ deleted items.</span></span> 
    
 <span data-ttu-id="488a9-118">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="488a9-118">_cEntDel_</span></span>
  
>  <span data-ttu-id="488a9-119">Out Die Anzahl der gelöschten Elemente im Ordner.</span><span class="sxs-lookup"><span data-stu-id="488a9-119">[out] Number of deleted items in the folder.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="488a9-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="488a9-120">See also</span></span>

- [<span data-ttu-id="488a9-121">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="488a9-121">About the Replication API</span></span>](about-the-replication-api.md) 
- [<span data-ttu-id="488a9-122">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="488a9-122">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="488a9-123">UPTBL</span><span class="sxs-lookup"><span data-stu-id="488a9-123">UPTBL</span></span>](uptbl.md)

