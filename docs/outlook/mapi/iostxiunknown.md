---
title: IOSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX
api_type:
- COM
ms.assetid: f374d8d9-be8e-2489-d5fe-8a92e0ecfc6f
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6d7de4d6c14179ddaba4e2ad907f1acc1c53b125
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431995"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="2286e-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2286e-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="2286e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2286e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2286e-105">Stellt Synchronisierungsmethoden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="2286e-105">Provides synchronization methods.</span></span> <span data-ttu-id="2286e-106">Diese Schnittstelle ruft die erforderlichen Informationen ab, um lokale Änderungen an den Server- und Serveränderungen im lokalen Speicher zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="2286e-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2286e-107">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="2286e-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="2286e-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="2286e-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="2286e-109">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2286e-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="2286e-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="2286e-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="2286e-111">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="2286e-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="2286e-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="2286e-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="2286e-113">Ruft erweiterte Informationen zum letzten Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="2286e-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="2286e-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="2286e-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="2286e-115">Informiert den lokalen Speicher darüber, dass die Synchronisierung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2286e-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="2286e-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="2286e-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="2286e-117">Bereitet den lokalen Speicher für die Synchronisierung in einem bestimmten Zustand vor und ruft die erforderlichen Informationen zum Replizieren ab.</span><span class="sxs-lookup"><span data-stu-id="2286e-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="2286e-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="2286e-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="2286e-119">Beendet die Synchronisierung im aktuellen Zustand und beendet den Status.</span><span class="sxs-lookup"><span data-stu-id="2286e-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="2286e-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="2286e-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="2286e-121">Startet die Synchronisierung für einen Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="2286e-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="2286e-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="2286e-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="2286e-123">Beendet die Synchronisierung für einen Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="2286e-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="2286e-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="2286e-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="2286e-125">Legt das Ergebnis der Synchronisierung fest.</span><span class="sxs-lookup"><span data-stu-id="2286e-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="2286e-126">*Platzhaltermitglied*</span><span class="sxs-lookup"><span data-stu-id="2286e-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="2286e-127">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="2286e-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2286e-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2286e-128">Remarks</span></span>

<span data-ttu-id="2286e-129">Wenn ein Client Ordner und Ordnerinhalte in einem lokalen Speicher hochlädt oder synchronisiert, verschiebt er den lokalen Speicher von einem Zustand in einen anderen, wie im Zustandsübergangsdiagramm in [Informationen](about-the-replication-state-machine.md)zum Replikationsstatuscomputer dargestellt.</span><span class="sxs-lookup"><span data-stu-id="2286e-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="2286e-130">Im Folgenden wird die Reihenfolge der Ereignisse für den Client zum Verschieben des lokalen Speichers von einem Zustand in einen anderen verwendet:</span><span class="sxs-lookup"><span data-stu-id="2286e-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="2286e-131">Der Client ruft **IOSTX::InitSync auf,** um den lokalen Speicher darüber zu informieren, dass die Replikation gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2286e-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="2286e-132">Abhängig von der Replikationsrichtung und den zu replizierenden Objekten ruft der Client **IOSTX::SyncBeg** auf, um die Replikation im entsprechenden Zustand zu starten.</span><span class="sxs-lookup"><span data-stu-id="2286e-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="2286e-133">Outlook stellt dem Client die erforderlichen Informationen zur Verfügung, und der Client führt die Replikation aus.</span><span class="sxs-lookup"><span data-stu-id="2286e-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="2286e-134">Der Client ruft **IOSTX::SetSyncResult auf,** um das Ergebnis der Replikation zurück zu geben.</span><span class="sxs-lookup"><span data-stu-id="2286e-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="2286e-135">Der Client ruft **IOSTX::SyncEnd** auf, um die Replikation zu beenden, Outlook die erforderlichen Informationen für die nachfolgende Replikation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="2286e-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="2286e-136">Insbesondere beim Herunterladen von Nachrichtenelementen verwendet der Client **IOSTX::SyncHdrBeg** und **IOSTX::SyncHdrEnd,** um ein vollständiges Nachrichtenelement mit dem Nachrichtenkopf im lokalen Speicher zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="2286e-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="2286e-137">Bei **IOSTX::SyncHdrBeg** wird der lokale Speicher in den Status "Nachrichtenkopf herunterladen" überwechselt.</span><span class="sxs-lookup"><span data-stu-id="2286e-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="2286e-138">Outlook stellt dem Client zunächst den aktuellen Nachrichtenkopf im lokalen Speicher zur.</span><span class="sxs-lookup"><span data-stu-id="2286e-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="2286e-139">Der Client lädt ein vollständiges Nachrichtenelement zusammen mit dem Nachrichtenkopf herunter.</span><span class="sxs-lookup"><span data-stu-id="2286e-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="2286e-140">Outlook das Element im lokalen Speicher mit dem vollständigen Nachrichtenelement aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="2286e-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="2286e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2286e-141">See also</span></span>



[<span data-ttu-id="2286e-142">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="2286e-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2286e-143">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="2286e-143">MAPI Constants</span></span>](mapi-constants.md)

