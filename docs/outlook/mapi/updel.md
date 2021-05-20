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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436800"
---
# <a name="updel"></a><span data-ttu-id="993f2-103">UPDEL</span><span class="sxs-lookup"><span data-stu-id="993f2-103">UPDEL</span></span>

  
  
<span data-ttu-id="993f2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="993f2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="993f2-105">Informationen zu Elementen, die in einem lokalen Speicher gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="993f2-105">Information for items that have been deleted in a local store.</span></span> <span data-ttu-id="993f2-106">Diese Informationen werden während des [Statusstatus zum Hochladen des Löschstatus verwendet.](upload-delete-status-state.md)</span><span class="sxs-lookup"><span data-stu-id="993f2-106">This information is used during the [upload delete status state](upload-delete-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="993f2-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="993f2-107">Quick info</span></span>

```cpp
struct UPDEL 
{ 
    PUPDELE pupde; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="993f2-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="993f2-108">Members</span></span>

 <span data-ttu-id="993f2-109">_pupde_</span><span class="sxs-lookup"><span data-stu-id="993f2-109">_pupde_</span></span>
  
>  <span data-ttu-id="993f2-110">[out] Vektor von [UPDELE-Einträgen.](updele.md)</span><span class="sxs-lookup"><span data-stu-id="993f2-110">[out] Vector of [UPDELE](updele.md) entries.</span></span> 
    
 <span data-ttu-id="993f2-111">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="993f2-111">_cEnt_</span></span>
  
> <span data-ttu-id="993f2-112">[out] Anzahl der Einträge in  *pupde*  .</span><span class="sxs-lookup"><span data-stu-id="993f2-112">[out] Number of entries in  *pupde*  .</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="993f2-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="993f2-113">See also</span></span>



[<span data-ttu-id="993f2-114">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="993f2-114">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="993f2-115">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="993f2-115">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="993f2-116">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="993f2-116">MAPI Constants</span></span>](mapi-constants.md)

