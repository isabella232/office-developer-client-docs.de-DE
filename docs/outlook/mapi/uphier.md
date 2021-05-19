---
title: UPHIER
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a75ca0dd-9c50-2a9f-6c59-1f8020833a01
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 45ef7ce9291376ac020035f0bde6172caf6cc01b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414921"
---
# <a name="uphier"></a><span data-ttu-id="604bd-103">UPHIER</span><span class="sxs-lookup"><span data-stu-id="604bd-103">UPHIER</span></span>
 
<span data-ttu-id="604bd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="604bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="604bd-105">Informationen zum Synchronisieren einer Ordnerhierarchie während des [Uploadhierarchiestatus](upload-hierarchy-state.md).</span><span class="sxs-lookup"><span data-stu-id="604bd-105">Information for synchronizing a folder hierarchy during the [upload hierarchy state](upload-hierarchy-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="604bd-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="604bd-106">Quick info</span></span>

```cpp
struct UPHIER 
{ 
    ULONG ulFlags; 
    LPSTREAM pstmReserved; 
    UINT iEnt; 
    UINT cEnt; 
};
```

## <a name="members"></a><span data-ttu-id="604bd-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="604bd-107">Members</span></span>

<span data-ttu-id="604bd-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="604bd-108">_ulFlags_</span></span>
  
> <span data-ttu-id="604bd-109">[in] Flags zum Ändern des Verhaltens beim Synchronisieren der Ordnerhierarchie.</span><span class="sxs-lookup"><span data-stu-id="604bd-109">[in] Flags to modify the behavior when synchronizing the folder hierarchy.</span></span>
    
  - <span data-ttu-id="604bd-110">UPH_OK</span><span class="sxs-lookup"><span data-stu-id="604bd-110">UPH_OK</span></span>
    
    - <span data-ttu-id="604bd-111">[in] Hochladen war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="604bd-111">[in] Upload was successful.</span></span> <span data-ttu-id="604bd-112">Der Client legt dies nach dem erfolgreichen Hochladen von Informationen auf den Server fest.</span><span class="sxs-lookup"><span data-stu-id="604bd-112">The client sets this after successfully uploading information to the server.</span></span> <span data-ttu-id="604bd-113">Wenn dieses Flag angezeigt wird, Outlook alle internen Buchhaltungsinformationen, die angegeben haben, dass die Ordnerhierarchie aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="604bd-113">Upon seeing this flag, Outlook clears any internal bookkeeping information that indicated the folder hierarchy needed updating.</span></span> 
    
    - <span data-ttu-id="604bd-114">Der Client übergibt das HRESULT, wenn der Upload nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="604bd-114">The client passes the HRESULT if the upload was not successful.</span></span>
    
<span data-ttu-id="604bd-115">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="604bd-115">_pstmReserved_</span></span>
  
> <span data-ttu-id="604bd-116">[out] Dieses Mitglied ist für die Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="604bd-116">[out] This member is reserved for Outlook internal use and is not supported.</span></span>
    
<span data-ttu-id="604bd-117">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="604bd-117">_iEnt_</span></span>
  
> <span data-ttu-id="604bd-118">[out] Index zum Nachverfolgen der Synchronisierung der durch *cEnt angegebenen Ordneranzahl.*</span><span class="sxs-lookup"><span data-stu-id="604bd-118">[out] Index to track synchronizing the number of folders specified by  *cEnt*  .</span></span> 
    
<span data-ttu-id="604bd-119">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="604bd-119">_cEnt_</span></span>
  
> <span data-ttu-id="604bd-120">[out] Die Anzahl der Ordner, die nicht synchronisiert sind.</span><span class="sxs-lookup"><span data-stu-id="604bd-120">[out] Number of folders that are out of sync.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="604bd-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="604bd-121">See also</span></span>

- [<span data-ttu-id="604bd-122">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="604bd-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="604bd-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="604bd-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="604bd-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="604bd-124">MAPI Constants</span></span>](mapi-constants.md)

