---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Letzte �nderung: Donnerstag, 5. Juli 2012'
ms.openlocfilehash: 51a79075dac62a051f5a28dbcb70e7d6ff200e65
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791618"
---
# <a name="dntble"></a><span data-ttu-id="31dc7-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="31dc7-103">DNTBLE</span></span>

  
  
<span data-ttu-id="31dc7-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="31dc7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="31dc7-105">Informationen für den Inhalt eines Ordners auf dem Server während der [Tabelle Downloadstatus](download-table-state.md)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="31dc7-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="31dc7-106">Dieser Download Prozess verwendet Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="31dc7-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="31dc7-107">Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="31dc7-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="31dc7-108">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="31dc7-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="31dc7-109">Members</span><span class="sxs-lookup"><span data-stu-id="31dc7-109">Members</span></span>

 <span data-ttu-id="31dc7-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="31dc7-110">_cEntNew_</span></span>
  
> <span data-ttu-id="31dc7-111">[out] Anzahl der Elemente im lokalen Speicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="31dc7-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="31dc7-112">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="31dc7-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="31dc7-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="31dc7-113">_cEntMod_</span></span>
  
> <span data-ttu-id="31dc7-114">[out] Anzahl der Elemente, die auf dem lokalen Speicher geändert.</span><span class="sxs-lookup"><span data-stu-id="31dc7-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="31dc7-115">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="31dc7-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="31dc7-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="31dc7-116">_cEntRead_</span></span>
  
> <span data-ttu-id="31dc7-117">[out] Anzahl der Elemente lesen oder auf dem lokalen Speicher als ungelesen markiert.</span><span class="sxs-lookup"><span data-stu-id="31dc7-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="31dc7-118">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="31dc7-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="31dc7-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="31dc7-119">_cEntDel_</span></span>
  
> <span data-ttu-id="31dc7-120">[out] Anzahl der Elemente, die auf dem lokalen Speicher gelöscht.</span><span class="sxs-lookup"><span data-stu-id="31dc7-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="31dc7-121">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="31dc7-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="31dc7-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31dc7-122">See also</span></span>



[<span data-ttu-id="31dc7-123">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="31dc7-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="31dc7-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="31dc7-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="31dc7-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="31dc7-125">DNTBL</span></span>](dntbl.md)

