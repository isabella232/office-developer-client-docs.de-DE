---
title: Status Synchronisieren
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7abbf049a848d417f640528e5030e37a954413e5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414627"
---
# <a name="synchronize-state"></a><span data-ttu-id="032fd-103">Status Synchronisieren</span><span class="sxs-lookup"><span data-stu-id="032fd-103">Synchronize State</span></span>

  
  
<span data-ttu-id="032fd-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="032fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="032fd-105">In diesem Thema wird beschrieben, was während des Synchronisierungsstatus des Replikationsstatus Computers passiert.</span><span class="sxs-lookup"><span data-stu-id="032fd-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="032fd-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="032fd-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="032fd-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="032fd-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="032fd-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="032fd-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="032fd-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="032fd-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="032fd-110">**[SYNCHRONISIERUNGS](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="032fd-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="032fd-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="032fd-111">From this state:</span></span>  <br/> |[<span data-ttu-id="032fd-112">Zustand „Leerlauf“</span><span class="sxs-lookup"><span data-stu-id="032fd-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="032fd-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="032fd-113">To this state:</span></span>  <br/> |<span data-ttu-id="032fd-114">[Download-Hierarchie Status](download-hierarchy-state.md), [Inhaltsstatus synchronisieren](synchronize-contents-state.md), Status der [Upload-Hierarchie](upload-hierarchy-state.md)oder Leerlaufstatus</span><span class="sxs-lookup"><span data-stu-id="032fd-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="032fd-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="032fd-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="032fd-116">Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="032fd-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="032fd-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="032fd-117">Description</span></span>

<span data-ttu-id="032fd-118">Dieser Status initiiert die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="032fd-118">This state initiates synchronization.</span></span> <span data-ttu-id="032fd-119">Ein lokaler Speicher kann von hier zu einem Upload-oder Downloadstatus wechseln.</span><span class="sxs-lookup"><span data-stu-id="032fd-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="032fd-120">Beispielsweise kann ein lokaler Speicher zum Upload-Hierarchie Status wechseln, um eine Ordnerhierarchie auf den Server hochzuladen, oder eine vollständige Synchronisierung durchführen, indem Sie zunächst die Hierarchie hochladen und dann die Hierarchie vom Server herunterladen.</span><span class="sxs-lookup"><span data-stu-id="032fd-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="032fd-121">Während dieses Status initialisiert Outlook die zugehörige **Synchronisierungs** Datenstruktur mit dem Pfad zum lokalen Speicher, sodass Outlook während anderer Statusänderungen sieht.</span><span class="sxs-lookup"><span data-stu-id="032fd-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="032fd-122">Der Client legt die [in]-Mitglieder der **Synchronisierung**fest, die Outlook anweist, wie andere Zustände behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="032fd-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="032fd-123">Der Client kann beispielsweise *ulFlags* auf **UPS_UPLOAD_ONLY** und **UPS_THESE_FOLDERS** und *PEL* auf eine Liste von Eintrags Bezeichnern der Ordner festlegen, um Outlook mitzuteilen, dass nur diese Ordner hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="032fd-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="032fd-124">Wenn dieser Status endet, wird der lokale Speicher in den Leerlauf zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="032fd-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="032fd-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="032fd-125">See also</span></span>



[<span data-ttu-id="032fd-126">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="032fd-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="032fd-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="032fd-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="032fd-128">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="032fd-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="032fd-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="032fd-129">SYNCSTATE</span></span>](syncstate.md)

