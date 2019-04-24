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
ms.openlocfilehash: c9d2ec7f1970e3d1cadb65ab9af360b5c01c6844
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360487"
---
# <a name="updel"></a><span data-ttu-id="b61b4-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="b61b4-103">UPDEL</span></span>

  
  
<span data-ttu-id="b61b4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b61b4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b61b4-105">Informationen zu Elementen, die in einem lokalen Speicher gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="b61b4-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="b61b4-106">Diese Informationen werden während des Status Status des [Uploads gelöscht](upload-delete-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="b61b4-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="b61b4-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b61b4-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="b61b4-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="b61b4-108">Members</span></span>

 <span data-ttu-id="b61b4-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="b61b4-109">_pupde_</span></span>
  
>  <span data-ttu-id="b61b4-110">Out Vektor der [UPdele](updele.md) -Einträge.</span><span class="sxs-lookup"><span data-stu-id="b61b4-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="b61b4-111">_Prozent_</span><span class="sxs-lookup"><span data-stu-id="b61b4-111">_cEnt_</span></span>
  
> <span data-ttu-id="b61b4-112">Out Anzahl der Einträge in *pupde* .</span><span class="sxs-lookup"><span data-stu-id="b61b4-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b61b4-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b61b4-113">See also</span></span>



[<span data-ttu-id="b61b4-114">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="b61b4-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b61b4-115">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="b61b4-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="b61b4-116">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b61b4-116">MAPI Constants</span></span>](mapi-constants.md)

