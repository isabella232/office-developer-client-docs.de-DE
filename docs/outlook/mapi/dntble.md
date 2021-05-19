---
title: DNTBLE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 10fb1650-6c3e-f467-91cd-48e5ddd82827
description: 'Letzte Änderung: 05. Juli 2012'
ms.openlocfilehash: 41a61bd05bd511888aeab756166016813f4dceb8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337114"
---
# <a name="dntble"></a><span data-ttu-id="9d6c4-103">DNTBLE</span><span class="sxs-lookup"><span data-stu-id="9d6c4-103">DNTBLE</span></span>

  
  
<span data-ttu-id="9d6c4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d6c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d6c4-105">Informationen zum Herunterladen der Inhalte eines Ordners vom Server während des [Download-Tabellenzustands](download-table-state.md).</span><span class="sxs-lookup"><span data-stu-id="9d6c4-105">Information for downloading the contents of a folder from the server during the [download table state](download-table-state.md).</span></span> <span data-ttu-id="9d6c4-106">Bei diesem Downloadvorgang wird Microsoft Exchange Incremental Change Synchronization (ICS) verwendet.</span><span class="sxs-lookup"><span data-stu-id="9d6c4-106">This downloading process uses Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="9d6c4-107">Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9d6c4-107">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="9d6c4-108">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="9d6c4-108">Quick info</span></span>

```cpp
struct DNTBLE 
{ 
    UINT cEntNew; 
    UINT cEntMod; 
    UINT cEntRead; 
    UINT cEntDel; 
};
```

## <a name="members"></a><span data-ttu-id="9d6c4-109">Elemente</span><span class="sxs-lookup"><span data-stu-id="9d6c4-109">Members</span></span>

 <span data-ttu-id="9d6c4-110">_cEntNew_</span><span class="sxs-lookup"><span data-stu-id="9d6c4-110">_cEntNew_</span></span>
  
> <span data-ttu-id="9d6c4-111">[out] Die Anzahl von Elementen, die dem lokalen Informationsspeichers hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="9d6c4-111">[out] Number of items added to the local store.</span></span> <span data-ttu-id="9d6c4-112">Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.</span><span class="sxs-lookup"><span data-stu-id="9d6c4-112">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="9d6c4-113">_cEntMod_</span><span class="sxs-lookup"><span data-stu-id="9d6c4-113">_cEntMod_</span></span>
  
> <span data-ttu-id="9d6c4-114">[out] Die Anzahl von Elementen, die im lokalen Informationsspeichers geändert wurden.</span><span class="sxs-lookup"><span data-stu-id="9d6c4-114">[out] Number of items modified on the local store.</span></span> <span data-ttu-id="9d6c4-115">Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.</span><span class="sxs-lookup"><span data-stu-id="9d6c4-115">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="9d6c4-116">_cEntRead_</span><span class="sxs-lookup"><span data-stu-id="9d6c4-116">_cEntRead_</span></span>
  
> <span data-ttu-id="9d6c4-117">[out] Die Anzahl von Elementen, die im lokalen Informationsspeichers als gelesen oder ungelesen markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9d6c4-117">[out] Number of items read or marked unread on the local store.</span></span> <span data-ttu-id="9d6c4-118">Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.</span><span class="sxs-lookup"><span data-stu-id="9d6c4-118">Outlook populates this value during the downloading when using ICS.</span></span>
    
 <span data-ttu-id="9d6c4-119">_cEntDel_</span><span class="sxs-lookup"><span data-stu-id="9d6c4-119">_cEntDel_</span></span>
  
> <span data-ttu-id="9d6c4-120">[out] Die Anzahl von Elementen, die im lokalen Informationsspeichers gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="9d6c4-120">[out] Number of items deleted on the local store.</span></span> <span data-ttu-id="9d6c4-121">Outlook füllt diesen Wert während des Herunterladens bei Verwendung von ICS aus.</span><span class="sxs-lookup"><span data-stu-id="9d6c4-121">Outlook populates this value during the downloading when using ICS.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9d6c4-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d6c4-122">See also</span></span>



[<span data-ttu-id="9d6c4-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="9d6c4-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="9d6c4-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9d6c4-124">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="9d6c4-125">DNTBL</span><span class="sxs-lookup"><span data-stu-id="9d6c4-125">DNTBL</span></span>](dntbl.md)

