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
ms.openlocfilehash: 2131197ca24804eec74270100fa70c05c47a27cc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410252"
---
# <a name="hdrsync"></a><span data-ttu-id="a1078-103">HDRSYNC</span><span class="sxs-lookup"><span data-stu-id="a1078-103">HDRSYNC</span></span>

  
  
<span data-ttu-id="a1078-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1078-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1078-105">Informationen zum Synchronisieren eines Nachrichtenkopfs während des [Status der Downloadnachrichtkopfzeile](download-message-header-state.md).</span><span class="sxs-lookup"><span data-stu-id="a1078-105">Information for synchronizing a message header during the [download message header state](download-message-header-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a1078-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a1078-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="a1078-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="a1078-107">Members</span></span>

 <span data-ttu-id="a1078-108">_pupmsg_</span><span class="sxs-lookup"><span data-stu-id="a1078-108">_pupmsg_</span></span>
  
- <span data-ttu-id="a1078-109">[out] Informationen für den aktuellen Nachrichtenkopf im lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="a1078-109">[out] Information for the current message header in the local store.</span></span>
    
 <span data-ttu-id="a1078-110">_feidPar_</span><span class="sxs-lookup"><span data-stu-id="a1078-110">_feidPar_</span></span>
  
- <span data-ttu-id="a1078-111">[out] Eintrags-ID für den übergeordneten Ordner des Nachrichtenelements.</span><span class="sxs-lookup"><span data-stu-id="a1078-111">[out] Entry ID for the parent folder of the message item.</span></span>
    
 <span data-ttu-id="a1078-112">_pstmReserved_</span><span class="sxs-lookup"><span data-stu-id="a1078-112">_pstmReserved_</span></span>
  
- <span data-ttu-id="a1078-113">[out] Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a1078-113">[out] This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="a1078-114">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a1078-114">_ulFlags_</span></span>
  
- <span data-ttu-id="a1078-115">[in] Flags zum Ändern des Verhaltens:</span><span class="sxs-lookup"><span data-stu-id="a1078-115">[in] Flags to modify behavior:</span></span>
    
- <span data-ttu-id="a1078-116">HSF_LOCAL</span><span class="sxs-lookup"><span data-stu-id="a1078-116">HSF_LOCAL</span></span>
    
  - <span data-ttu-id="a1078-117">[in] Das vollständige Element befindet sich im gleichen lokalen Speicher wie das Kopfzeilenelement.</span><span class="sxs-lookup"><span data-stu-id="a1078-117">[in] Full item resides in the same local store as the header item.</span></span>
    
- <span data-ttu-id="a1078-118">HSF_COPYDESTRUCTIVE</span><span class="sxs-lookup"><span data-stu-id="a1078-118">HSF_COPYDESTRUCTIVE</span></span>
    
  -  <span data-ttu-id="a1078-119">[in] Optimieren sie interne Kopiervorgänge.</span><span class="sxs-lookup"><span data-stu-id="a1078-119">[in] Optimize internal copy operations.</span></span> <span data-ttu-id="a1078-120">Dies kann zu Datenverlusten führen.</span><span class="sxs-lookup"><span data-stu-id="a1078-120">This might cause data loss.</span></span> <span data-ttu-id="a1078-121">**HSF_LOCAL** muss festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a1078-121">**HSF_LOCAL** must be set.</span></span> 
    
- <span data-ttu-id="a1078-122">HSF_OK</span><span class="sxs-lookup"><span data-stu-id="a1078-122">HSF_OK</span></span>
    
  - <span data-ttu-id="a1078-123">[in] Die Kopfzeilensynchronisierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a1078-123">[in] Header synchronization was successful.</span></span> <span data-ttu-id="a1078-124">Der Client legt dies nach dem Herunterladen von Informationen vom Server fest.</span><span class="sxs-lookup"><span data-stu-id="a1078-124">The client sets this after downloading information from the server.</span></span>
    
     <span data-ttu-id="a1078-125">_pmsgFull_</span><span class="sxs-lookup"><span data-stu-id="a1078-125">_pmsgFull_</span></span>
    
  - <span data-ttu-id="a1078-126">[in] Das vollständige Nachrichtenelement einschließlich des Nachrichtenkopfs, der vom Server heruntergeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="a1078-126">[in] The full message item including the message header downloaded from the server.</span></span> <span data-ttu-id="a1078-127">Die Typdefinition von **LPMESSAGE** finden Sie unter mapidefs.h.</span><span class="sxs-lookup"><span data-stu-id="a1078-127">See mapidefs.h for the type definition of **LPMESSAGE**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a1078-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1078-128">See also</span></span>



[<span data-ttu-id="a1078-129">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="a1078-129">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a1078-130">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="a1078-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a1078-131">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a1078-131">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a1078-132">FEID</span><span class="sxs-lookup"><span data-stu-id="a1078-132">FEID</span></span>](feid.md)

