---
title: Nachrichtenkopfstatus herunterladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417119"
---
# <a name="download-message-header-state"></a><span data-ttu-id="117de-103">Nachrichtenkopfstatus herunterladen</span><span class="sxs-lookup"><span data-stu-id="117de-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="117de-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="117de-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="117de-105">In diesem Thema wird beschrieben, was während des Nachrichtenkopfstatus des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="117de-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="117de-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="117de-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="117de-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="117de-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="117de-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="117de-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="117de-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="117de-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="117de-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="117de-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="117de-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="117de-111">From this state:</span></span>  <br/> |[<span data-ttu-id="117de-112">Zustand „Leerlauf“</span><span class="sxs-lookup"><span data-stu-id="117de-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="117de-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="117de-113">To this state:</span></span>  <br/> |<span data-ttu-id="117de-114">Zustand „Leerlauf“</span><span class="sxs-lookup"><span data-stu-id="117de-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="117de-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="117de-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="117de-116">Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="117de-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="117de-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="117de-117">Description</span></span>

<span data-ttu-id="117de-118">Während dieses Zustands aktualisiert der Client den Header einer Nachricht in einem lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="117de-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="117de-119">Der lokale Speicher tritt diesen Status bei **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** ein und wird beendet, wenn **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="117de-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="117de-120">Während dieses Status initialisiert Outlook Elemente der zugeordneten **HDRSYNC-Datenstruktur** mit Informationen zum Kopf einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="117de-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="117de-121">Der Client lädt zuerst das vollständige Nachrichtenelement vom Server herunter und aktualisiert dann die Kopfzeile des Nachrichtenelements lokal.</span><span class="sxs-lookup"><span data-stu-id="117de-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="117de-122">Wenn die Syncrhonisierung endet, legt der Client die Downloadergebnisse fest.</span><span class="sxs-lookup"><span data-stu-id="117de-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="117de-123">Der lokale Speicher kehrt in den Leerlaufzustand zurück.</span><span class="sxs-lookup"><span data-stu-id="117de-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="117de-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="117de-124">See also</span></span>



[<span data-ttu-id="117de-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="117de-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="117de-126">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="117de-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="117de-127">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="117de-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="117de-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="117de-128">SYNCSTATE</span></span>](syncstate.md)

