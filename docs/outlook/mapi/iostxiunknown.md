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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7419a0df7a2f3b76caeeb1ca564624d437eddd52
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792735"
---
# <a name="iostx--iunknown"></a><span data-ttu-id="b3196-103">IOSTX: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3196-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="b3196-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b3196-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b3196-105">Stellt Synchronisierungsmethoden bereit.</span><span class="sxs-lookup"><span data-stu-id="b3196-105">Provides synchronization methods.</span></span> <span data-ttu-id="b3196-106">Diese Schnittstelle ruft die erforderlichen Informationen zum Replizieren von lokaler Änderungen auf den Server und Server Änderungen an den lokalen Speicher ab.</span><span class="sxs-lookup"><span data-stu-id="b3196-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b3196-107">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="b3196-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="b3196-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="b3196-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="b3196-109">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="b3196-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="b3196-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="b3196-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="b3196-111">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="b3196-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="b3196-112">GetLastError</span><span class="sxs-lookup"><span data-stu-id="b3196-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="b3196-113">Ruft Informationen über den letzten Fehler erweitert.</span><span class="sxs-lookup"><span data-stu-id="b3196-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="b3196-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="b3196-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="b3196-115">Informiert dem lokalen Speicher, dass Synchronisierung gestartet.</span><span class="sxs-lookup"><span data-stu-id="b3196-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="b3196-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="b3196-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="b3196-117">Bereitet den lokalen Speicher für die Synchronisierung in einen bestimmten Status und die erforderliche Informationen zum Replizieren von abgerufen.</span><span class="sxs-lookup"><span data-stu-id="b3196-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="b3196-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="b3196-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="b3196-119">Synchronisierung in den aktuellen Status beendet und diesen Status beendet.</span><span class="sxs-lookup"><span data-stu-id="b3196-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="b3196-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="b3196-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="b3196-121">Synchronisierung für ein Nachrichtenkopf gestartet.</span><span class="sxs-lookup"><span data-stu-id="b3196-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="b3196-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="b3196-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="b3196-123">Synchronisierung für ein Nachrichtenkopf endet.</span><span class="sxs-lookup"><span data-stu-id="b3196-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="b3196-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="b3196-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="b3196-125">Das Ergebnis der Synchronisierung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b3196-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="b3196-126">*Platzhalter-member*</span><span class="sxs-lookup"><span data-stu-id="b3196-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="b3196-127">*Nicht unterstützte oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="b3196-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b3196-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b3196-128">Remarks</span></span>

<span data-ttu-id="b3196-129">Wenn ein Client hochgeladen oder Ordner und Ordnerinhalte in einem lokalen Speicher synchronisiert, verschiebt es den lokalen Speicher von einem Zustand zu einem anderen wie in der Statusübergangsdiagramm in [Über die Replikation Zustandsautomat](about-the-replication-state-machine.md)dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b3196-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="b3196-130">Es folgt der Reihenfolge von Ereignissen für den Client auf den lokalen Speicher von einem Zustand in einen anderen verschieben:</span><span class="sxs-lookup"><span data-stu-id="b3196-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="b3196-131">Der Client ruft **IOSTX::InitSync** , um dem lokalen Speicher zu informieren, dass die Replikation zu starten.</span><span class="sxs-lookup"><span data-stu-id="b3196-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="b3196-132">Abhängig von der Richtung der Replikation und die Objekte repliziert werden ruft der Client **IOSTX::SyncBeg** , um die Replikation in den entsprechenden Status zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="b3196-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="b3196-133">Outlook bietet des Clients die erforderliche Informationen und der Client führt die Replikation.</span><span class="sxs-lookup"><span data-stu-id="b3196-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="b3196-134">Der Client ruft **IOSTX::SetSyncResult** , um das Ergebnis der Replikation zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="b3196-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="b3196-135">Der Client ruft **IOSTX::SyncEnd** zum Beenden der Replikations Outlook die erforderliche Informationen für die nachfolgende Replikation bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b3196-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="b3196-136">Insbesondere verwendet beim Download von Nachrichtenelemente der Client **IOSTX::SyncHdrBeg** und **IOSTX::SyncHdrEnd** so aktualisieren Sie eine vollständige e-Mail-Element mit der Nachrichtenkopf auf dem lokalen Speicher:</span><span class="sxs-lookup"><span data-stu-id="b3196-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="b3196-137">Bei **IOSTX::SyncHdrBeg**Speichern der lokalen Kopie Übergänge in den Downloadstatus der Nachricht Kopfzeile.</span><span class="sxs-lookup"><span data-stu-id="b3196-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="b3196-138">Outlook ermöglicht dem Client mit der aktuellen Nachrichtenkopf anfangs auf dem lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="b3196-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="b3196-139">Der Client finden Sie eine vollständige e-Mail-Element zusammen mit der Nachrichtenkopf downloads.</span><span class="sxs-lookup"><span data-stu-id="b3196-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="b3196-140">Outlook aktualisiert das Element auf dem lokalen Speicher mit dem vollständigen Nachrichtenelement.</span><span class="sxs-lookup"><span data-stu-id="b3196-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b3196-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3196-141">See also</span></span>



[<span data-ttu-id="b3196-142">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="b3196-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="b3196-143">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b3196-143">MAPI Constants</span></span>](mapi-constants.md)

