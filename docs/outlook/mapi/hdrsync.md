---
title: HDRSYNC
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bf6892d0-a923-e926-5361-59efa49ebdc0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bd1c327eb2042957c8fb043736950af3dae520b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791827"
---
# <a name="hdrsync"></a><span data-ttu-id="456dd-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="456dd-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="456dd-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="456dd-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="456dd-105">Informationen zum Synchronisieren von Nachrichtenkopfzeile während der [Status der Nachricht Kopfzeilen herunterladen](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="456dd-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="456dd-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="456dd-106">Quick info</span></span>

```cpp
struct HDRSYNC 
{ 
    UPMSG *pupmsg; 
    FEID feidPar; 
    LPSTREAM pstmReserved; 
    ULONG ulFlags; 
    LPMESSAGE pmsgFull; 
};
```

## <a name="members"></a><span data-ttu-id="456dd-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="456dd-107">Members</span></span>

 <span data-ttu-id="456dd-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="456dd-108">_pupmsg_</span></span>
  
- <span data-ttu-id="456dd-109">[out] Informationen für die aktuelle Nachrichtenkopfzeile in den lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="456dd-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="456dd-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="456dd-110">_feidPar_</span></span>
  
- <span data-ttu-id="456dd-111">[out] Eintrags-ID für den übergeordneten Ordner des Nachrichtenobjekts.</span><span class="sxs-lookup"><span data-stu-id="456dd-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="456dd-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="456dd-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="456dd-113">[out] Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="456dd-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="456dd-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="456dd-114">_ulFlags_</span></span>
  
- <span data-ttu-id="456dd-115">[in] Flags, Verhalten zu ändern:</span><span class="sxs-lookup"><span data-stu-id="456dd-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="456dd-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="456dd-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="456dd-117">[in] Vollständige Element befindet sich im gleichen lokalen Speicher als Headerelement.</span><span class="sxs-lookup"><span data-stu-id="456dd-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="456dd-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="456dd-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="456dd-119">[in] Interne Copy-Vorgänge zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="456dd-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="456dd-120">Dies kann zu Datenverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="456dd-120">This might cause data loss.</span></span> <span data-ttu-id="456dd-121">**HSF_LOCAL** muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="456dd-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="456dd-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="456dd-122">HSF_OK</span></span>
    
  - <span data-ttu-id="456dd-123">[in] Header-Synchronisierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="456dd-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="456dd-124">Der Client legt dies nach dem Herunterladen von Informationen vom Server.</span><span class="sxs-lookup"><span data-stu-id="456dd-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="456dd-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="456dd-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="456dd-126">[in] Das vollständige e-Mail-Element mit der Kopfzeile, die vom Server heruntergeladen werden.</span><span class="sxs-lookup"><span data-stu-id="456dd-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="456dd-127">Finden Sie unter mapidefs.h für die Definition des **LPMESSAGE**Typs.</span><span class="sxs-lookup"><span data-stu-id="456dd-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="456dd-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="456dd-128">See also</span></span>



[<span data-ttu-id="456dd-129">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="456dd-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="456dd-130">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="456dd-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="456dd-131">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="456dd-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="456dd-132">FEID</span><span class="sxs-lookup"><span data-stu-id="456dd-132">FEID</span></span>](feid.md)

