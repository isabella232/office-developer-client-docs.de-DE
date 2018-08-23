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
ms.openlocfilehash: d92e8d7b3fb14051ffceb829f3df3f6fa12e6e23
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565858"
---
# <a name="dntble"></a><span data-ttu-id="ea7ab-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="ea7ab-103">DNTBLE</span></span>

  
  
<span data-ttu-id="ea7ab-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ea7ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ea7ab-105">Informationen für den Inhalt eines Ordners auf dem Server während der [Tabelle Downloadstatus](download-table-state.md)herunterladen.</span><span class="sxs-lookup"><span data-stu-id="ea7ab-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="ea7ab-106">Dieser Download Prozess verwendet Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="ea7ab-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="ea7ab-107">Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ea7ab-107">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ea7ab-108">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ea7ab-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="ea7ab-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="ea7ab-109">Members</span></span>

 <span data-ttu-id="ea7ab-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="ea7ab-110">_cEntNew_</span></span>
  
> <span data-ttu-id="ea7ab-111">[out] Anzahl der Elemente im lokalen Speicher hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ea7ab-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="ea7ab-112">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="ea7ab-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="ea7ab-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="ea7ab-113">_cEntMod_</span></span>
  
> <span data-ttu-id="ea7ab-114">[out] Anzahl der Elemente, die auf dem lokalen Speicher geändert.</span><span class="sxs-lookup"><span data-stu-id="ea7ab-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="ea7ab-115">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="ea7ab-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="ea7ab-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="ea7ab-116">_cEntRead_</span></span>
  
> <span data-ttu-id="ea7ab-117">[out] Anzahl der Elemente lesen oder auf dem lokalen Speicher als ungelesen markiert.</span><span class="sxs-lookup"><span data-stu-id="ea7ab-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="ea7ab-118">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="ea7ab-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="ea7ab-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="ea7ab-119">_cEntDel_</span></span>
  
> <span data-ttu-id="ea7ab-120">[out] Anzahl der Elemente, die auf dem lokalen Speicher gelöscht.</span><span class="sxs-lookup"><span data-stu-id="ea7ab-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="ea7ab-121">Outlook wird dieser Wert während des Herunterladens, bei Verwendung von ICS aufgefüllt.</span><span class="sxs-lookup"><span data-stu-id="ea7ab-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ea7ab-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea7ab-122">See also</span></span>



[<span data-ttu-id="ea7ab-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="ea7ab-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ea7ab-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ea7ab-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ea7ab-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="ea7ab-125">DNTBL</span></span>](dntbl.md)

