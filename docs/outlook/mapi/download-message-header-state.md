---
title: Status „Downloadnachrichtenkopf“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 03f69592-a5ea-e30b-9674-9cfa895163d8
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7407b6606634ecc0151f582e4481ecbff5e7dc57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791574"
---
# <a name="download-message-header-state"></a><span data-ttu-id="c9938-103">Status „Downloadnachrichtenkopf“</span><span class="sxs-lookup"><span data-stu-id="c9938-103">Download Message Header State</span></span>

  
  
<span data-ttu-id="c9938-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c9938-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="c9938-105">In diesem Thema wird beschrieben, was geschieht, während die Nachricht Header-Downloadstatus von der Replikation Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="c9938-105">This topic describes what happens during the download message header state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="c9938-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c9938-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9938-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="c9938-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="c9938-108">**LR_SYNC_DOWNLOAD_HEADER**</span><span class="sxs-lookup"><span data-stu-id="c9938-108">**LR_SYNC_DOWNLOAD_HEADER**</span></span> <br/> |
|<span data-ttu-id="c9938-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="c9938-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="c9938-110">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="c9938-110">**[HDRSYNC](hdrsync.md)**</span></span> <br/> |
|<span data-ttu-id="c9938-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="c9938-111">From this state:</span></span>  <br/> |[<span data-ttu-id="c9938-112">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="c9938-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="c9938-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="c9938-113">To this state:</span></span>  <br/> |<span data-ttu-id="c9938-114">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="c9938-114">Idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="c9938-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="c9938-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="c9938-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="c9938-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="c9938-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9938-117">Description</span></span>

<span data-ttu-id="c9938-118">Während dieser Status aktualisiert den Client die Kopfzeile einer Nachricht in einem lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="c9938-118">During this state, the client updates the header of a message on a local store.</span></span> <span data-ttu-id="c9938-119">Der lokale Speicher gibt diesen Zustand bei **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** und wird beendet, wenn **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c9938-119">The local store enters this state upon **[IOSTX::SyncHdrBeg](iostx-synchdrbeg.md)** and exits when **[IOSTX::SyncHdrEnd](iostx-synchdrend.md)** is called.</span></span> <span data-ttu-id="c9938-120">Während dieser Zustand initialisiert Outlook Mitglieder der zugeordneten **HDRSYNC** -Datenstruktur mit Informationen über die Kopfzeile einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c9938-120">During this state, Outlook initializes members of the associated **HDRSYNC** data structure with information about the header of a message.</span></span> <span data-ttu-id="c9938-121">Der Client zunächst das vollständige e-Mail-Element vom Server heruntergeladen und aktualisiert anschließend die Kopfzeile des Nachrichtenelements lokal.</span><span class="sxs-lookup"><span data-stu-id="c9938-121">The client first downloads the full message item from the server and then updates the header of the message item locally.</span></span> 
  
<span data-ttu-id="c9938-122">Am Ende des [v2], wird der Client die Ergebnisse herunterladen.</span><span class="sxs-lookup"><span data-stu-id="c9938-122">When syncrhonization ends, the client sets the download results.</span></span> <span data-ttu-id="c9938-123">In den Leerlauf gibt der lokale Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="c9938-123">The local store returns to the idle state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c9938-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9938-124">See also</span></span>



[<span data-ttu-id="c9938-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="c9938-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c9938-126">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="c9938-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="c9938-127">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="c9938-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c9938-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="c9938-128">SYNCSTATE</span></span>](syncstate.md)

