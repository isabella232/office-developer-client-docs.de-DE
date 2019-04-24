---
title: Nachrichtenkopf Status herunterladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c8e83119d724f583d40583a6a5227bc467dc94da
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338836"
---
# <a name="download-message-header-state"></a><span data-ttu-id="3a9db-103">Nachrichtenkopf Status herunterladen</span><span class="sxs-lookup"><span data-stu-id="3a9db-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="3a9db-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a9db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="3a9db-105">In diesem Thema wird beschrieben, was während des Download Nachrichtenkopf Status des Replikationsstatus Computers passiert.</span><span class="sxs-lookup"><span data-stu-id="3a9db-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3a9db-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="3a9db-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3a9db-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="3a9db-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="3a9db-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="3a9db-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="3a9db-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="3a9db-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="3a9db-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="3a9db-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="3a9db-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="3a9db-111">From this state:</span></span>  <br/> |[<span data-ttu-id="3a9db-112">Zustand „Leerlauf“</span><span class="sxs-lookup"><span data-stu-id="3a9db-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="3a9db-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="3a9db-113">To this state:</span></span>  <br/> |<span data-ttu-id="3a9db-114">Zustand „Leerlauf“</span><span class="sxs-lookup"><span data-stu-id="3a9db-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="3a9db-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="3a9db-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="3a9db-116">Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="3a9db-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="3a9db-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a9db-117">Description</span></span>

<span data-ttu-id="3a9db-118">Während dieses Status aktualisiert der Client die Kopfzeile einer Nachricht in einem lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="3a9db-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="3a9db-119">Der lokale Speicher gibt diesen Status bei **[IOSTX:: SyncHdrBeg](iostx-synchdrbeg.md)** und Exits ein, wenn **[IOSTX:: SyncHdrEnd](iostx-synchdrend.md)** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3a9db-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="3a9db-120">Während dieses Status initialisiert Outlook Member der zugeordneten **HDRSYNC** -Datenstruktur mit Informationen über die Kopfzeile einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="3a9db-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="3a9db-121">Der Client downloadet zunächst das vollständige Nachrichtenelement vom Server und aktualisiert dann die Kopfzeile des Nachrichtenelements lokal.</span><span class="sxs-lookup"><span data-stu-id="3a9db-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="3a9db-122">Wenn Synchronisation endet, legt der Client die Download Ergebnisse fest.</span><span class="sxs-lookup"><span data-stu-id="3a9db-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="3a9db-123">Der lokale Speicher wird in den Leerlauf zurückversetzt.</span><span class="sxs-lookup"><span data-stu-id="3a9db-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3a9db-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a9db-124">See also</span></span>



[<span data-ttu-id="3a9db-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="3a9db-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3a9db-126">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3a9db-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3a9db-127">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="3a9db-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="3a9db-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="3a9db-128">SYNCSTATE</span></span>](syncstate.md)

