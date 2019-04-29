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
# <a name="iostx--iunknown"></a><span data-ttu-id="cefef-103">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cefef-103">IOSTX : IUnknown</span></span>

  
  
<span data-ttu-id="cefef-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cefef-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cefef-105">Stellt Synchronisierungsmethoden bereit.</span><span class="sxs-lookup"><span data-stu-id="cefef-105">Provides synchronization methods.</span></span> <span data-ttu-id="cefef-106">Diese Schnittstelle ruft die erforderlichen Informationen ab, um lokale Änderungen an den Server-und Server Änderungen im lokalen Speicher zu replizieren.</span><span class="sxs-lookup"><span data-stu-id="cefef-106">This interface retrieves the necessary information to replicate local changes to the server and server changes to the local store.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="cefef-107">Bereitgestellt von:</span><span class="sxs-lookup"><span data-stu-id="cefef-107">Provided by:</span></span>  <br/> |[<span data-ttu-id="cefef-108">IPSTX::GetSyncObject</span><span class="sxs-lookup"><span data-stu-id="cefef-108">IPSTX::GetSyncObject</span></span>](iostx-setsyncresult.md) <br/> |
|<span data-ttu-id="cefef-109">Schnittstellenbezeichner:</span><span class="sxs-lookup"><span data-stu-id="cefef-109">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cefef-110">IID_IOSTX</span><span class="sxs-lookup"><span data-stu-id="cefef-110">IID_IOSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cefef-111">Vtable-Reihenfolge</span><span class="sxs-lookup"><span data-stu-id="cefef-111">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cefef-112">Getlasterroraufzurufen</span><span class="sxs-lookup"><span data-stu-id="cefef-112">GetLastError</span></span>](iostx-getlasterror.md) <br/> |<span data-ttu-id="cefef-113">Ruft erweiterte Informationen zum letzten Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="cefef-113">Gets extended information about the last error.</span></span>  <br/> |
|[<span data-ttu-id="cefef-114">InitSync</span><span class="sxs-lookup"><span data-stu-id="cefef-114">InitSync</span></span>](iostx-initsync.md) <br/> |<span data-ttu-id="cefef-115">Informiert den lokalen Speicher über die Synchronisierung, die gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cefef-115">Informs the local store that synchronization is about to start.</span></span>  <br/> |
|[<span data-ttu-id="cefef-116">SyncBeg</span><span class="sxs-lookup"><span data-stu-id="cefef-116">SyncBeg</span></span>](iostx-syncbeg.md) <br/> |<span data-ttu-id="cefef-117">Bereitet den lokalen Speicher für die Synchronisierung in einem bestimmten Zustand vor und ruft die erforderlichen Informationen zum Replizieren ab.</span><span class="sxs-lookup"><span data-stu-id="cefef-117">Prepares the local store for synchronization in a particular state and retrieves the necessary information to replicate.</span></span>  <br/> |
|[<span data-ttu-id="cefef-118">SyncEnd</span><span class="sxs-lookup"><span data-stu-id="cefef-118">SyncEnd</span></span>](iostx-syncend.md) <br/> |<span data-ttu-id="cefef-119">Beendet die Synchronisierung im aktuellen Zustand und beendet diesen Status.</span><span class="sxs-lookup"><span data-stu-id="cefef-119">Ends synchronization in the current state and exits that state.</span></span>  <br/> |
|[<span data-ttu-id="cefef-120">SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="cefef-120">SyncHdrBeg</span></span>](iostx-synchdrbeg.md) <br/> |<span data-ttu-id="cefef-121">Startet die Synchronisierung für einen Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="cefef-121">Starts synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="cefef-122">SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="cefef-122">SyncHdrEnd</span></span>](iostx-synchdrend.md) <br/> |<span data-ttu-id="cefef-123">Beendet die Synchronisierung für einen Nachrichtenkopf.</span><span class="sxs-lookup"><span data-stu-id="cefef-123">Ends synchronization for a message header.</span></span>  <br/> |
|[<span data-ttu-id="cefef-124">SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="cefef-124">SetSyncResult</span></span>](iostx-setsyncresult.md) <br/> |<span data-ttu-id="cefef-125">Legt das Ergebnis der Synchronisierung fest.</span><span class="sxs-lookup"><span data-stu-id="cefef-125">Sets the result of the synchronization.</span></span>  <br/> |
| <span data-ttu-id="cefef-126">*Platzhalterelement*</span><span class="sxs-lookup"><span data-stu-id="cefef-126">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="cefef-127">*Nicht unterstützt oder dokumentiert.*</span><span class="sxs-lookup"><span data-stu-id="cefef-127">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cefef-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cefef-128">Remarks</span></span>

<span data-ttu-id="cefef-129">Wenn ein Clientordner und Ordnerinhalte in einem lokalen Speicher hochlädt oder synchronisiert, verschiebt er den lokalen Speicher von einem Status in einen anderen, wie er im Zustandsübergang-Diagramm in [über den Replikationsstatus Computer](about-the-replication-state-machine.md)dargestellt ist.</span><span class="sxs-lookup"><span data-stu-id="cefef-129">When a client uploads or synchronizes folders and folder contents on a local store, it moves the local store from one state to another as depicted in the state transition diagram in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="cefef-130">Im folgenden finden Sie die Reihenfolge der Ereignisse für den Client zum Verschieben des lokalen Speichers von einem Status in einen anderen:</span><span class="sxs-lookup"><span data-stu-id="cefef-130">The following is the order of events for the client to move the local store from one state to another:</span></span>
  
1. <span data-ttu-id="cefef-131">Der Client ruft **IOSTX:: InitSync** auf, um den lokalen Speicher zu informieren, dass die Replikation gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="cefef-131">The client calls **IOSTX::InitSync** to inform the local store that replication is about to start.</span></span> 
    
2. <span data-ttu-id="cefef-132">Abhängig von der Replikationsrichtung und den zu replizierenden Objekten ruft der Client **IOSTX:: SyncBeg** auf, um die Replikation im entsprechenden Zustand zu starten.</span><span class="sxs-lookup"><span data-stu-id="cefef-132">Depending on the direction of replication and the objects to replicate, the client calls **IOSTX::SyncBeg** to begin replication in the appropriate state.</span></span> <span data-ttu-id="cefef-133">Outlook stellt dem Client die erforderlichen Informationen bereit, und der Client führt die Replikation aus.</span><span class="sxs-lookup"><span data-stu-id="cefef-133">Outlook provides the client the necessary information, and the client performs the replication.</span></span> 
    
3. <span data-ttu-id="cefef-134">Der Client ruft **IOSTX:: SetSyncResult** auf, um das Ergebnis der Replikation zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="cefef-134">The client calls **IOSTX::SetSyncResult** to return the result of the replication.</span></span> 
    
4. <span data-ttu-id="cefef-135">Der Client ruft **IOSTX:: SyncEnd** auf, um die Replikation zu beenden, sodass Outlook die erforderlichen Informationen für die nachfolgende Replikation bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cefef-135">The client calls **IOSTX::SyncEnd** to end the replication, providing Outlook the necessary information for subsequent replication.</span></span> 
    
<span data-ttu-id="cefef-136">Insbesondere verwendet der Client beim Herunterladen von Nachrichtenelementen **IOSTX:: SyncHdrBeg** und **IOSTX:: SyncHdrEnd** , um ein vollständiges Nachrichtenelement mit dem Nachrichtenkopf im lokalen Speicher zu aktualisieren:</span><span class="sxs-lookup"><span data-stu-id="cefef-136">In particular, when downloading message items, the client uses **IOSTX::SyncHdrBeg** and **IOSTX::SyncHdrEnd** to update a full message item with the message header on the local store:</span></span> 
  
1. <span data-ttu-id="cefef-137">Bei **IOSTX:: SyncHdrBeg**wechselt der lokale Speicher in den Status des Download Nachrichtenkopfs.</span><span class="sxs-lookup"><span data-stu-id="cefef-137">Upon **IOSTX::SyncHdrBeg**, the local store transitions into the download message header state.</span></span> <span data-ttu-id="cefef-138">Outlook stellt dem Client anfänglich den aktuellen Nachrichtenkopf des lokalen Speichers zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cefef-138">Outlook initially provides the client with the current message header on the local store.</span></span>
    
2. <span data-ttu-id="cefef-139">Der Client lädt ein vollständiges Nachrichtenelement zusammen mit dem Nachrichtenkopf herunter.</span><span class="sxs-lookup"><span data-stu-id="cefef-139">The client downloads a full message item together with the message header.</span></span>
    
3. <span data-ttu-id="cefef-140">Outlook aktualisiert das Element im lokalen Speicher mit dem vollständigen Nachrichtenelement.</span><span class="sxs-lookup"><span data-stu-id="cefef-140">Outlook updates the item on the local store with the full message item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cefef-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cefef-141">See also</span></span>



[<span data-ttu-id="cefef-142">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="cefef-142">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="cefef-143">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="cefef-143">MAPI Constants</span></span>](mapi-constants.md)

