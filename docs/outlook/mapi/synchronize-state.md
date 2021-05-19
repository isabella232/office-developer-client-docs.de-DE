---
title: Synchronisierungsstatus
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
# <a name="synchronize-state"></a><span data-ttu-id="2be16-103">Synchronisierungsstatus</span><span class="sxs-lookup"><span data-stu-id="2be16-103">Synchronize State</span></span>

  
  
<span data-ttu-id="2be16-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2be16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2be16-105">In diesem Thema wird beschrieben, was während des Synchronisierungsstatus des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="2be16-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2be16-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2be16-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2be16-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2be16-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="2be16-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="2be16-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="2be16-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="2be16-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="2be16-110">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="2be16-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="2be16-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="2be16-111">From this state:</span></span>  <br/> |[<span data-ttu-id="2be16-112">Zustand „Leerlauf“</span><span class="sxs-lookup"><span data-stu-id="2be16-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="2be16-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="2be16-113">To this state:</span></span>  <br/> |<span data-ttu-id="2be16-114">[Downloadhierarchiestatus,](download-hierarchy-state.md) [Inhaltsstatus synchronisieren,](synchronize-contents-state.md) [Uploadhierarchiestatus](upload-hierarchy-state.md)oder Leerlaufzustand</span><span class="sxs-lookup"><span data-stu-id="2be16-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="2be16-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="2be16-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="2be16-116">Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="2be16-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="2be16-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2be16-117">Description</span></span>

<span data-ttu-id="2be16-118">Dieser Zustand initiiert die Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="2be16-118">This state initiates synchronization.</span></span> <span data-ttu-id="2be16-119">Ein lokaler Speicher kann von hier aus zu einem Upload- oder Downloadstatus überwechseln.</span><span class="sxs-lookup"><span data-stu-id="2be16-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="2be16-120">Beispielsweise kann ein lokaler Speicher in den Uploadhierarchiestatus wechseln, um eine Ordnerhierarchie auf den Server hochzuladen, oder er kann eine vollständige Synchronisierung durchführen, indem er zuerst die Hierarchie hoch- und dann die Hierarchie vom Server herunterloaden.</span><span class="sxs-lookup"><span data-stu-id="2be16-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="2be16-121">Während dieses Status initialisiert Outlook die  zugeordnete SYNC-Datenstruktur mit dem Pfad zum lokalen Speicher, sodass Outlook änderungen während anderer Zustände sehen.</span><span class="sxs-lookup"><span data-stu-id="2be16-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="2be16-122">Der Client legt die [in]-Mitglieder von **SYNC** fest, die Outlook wie andere Zustände zu behandeln sind.</span><span class="sxs-lookup"><span data-stu-id="2be16-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="2be16-123">Beispielsweise kann der Client *ulFlags* auf **UPS_UPLOAD_ONLY** und **UPS_THESE_FOLDERS** und *pel* auf eine Liste der Eintragsbezeichner der Ordner festlegen, um Outlook zu informieren, dass nur diese Ordner hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="2be16-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="2be16-124">Wenn dieser Zustand endet, wird der lokale Speicher in den Leerlaufzustand zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="2be16-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2be16-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2be16-125">See also</span></span>



[<span data-ttu-id="2be16-126">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="2be16-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2be16-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="2be16-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2be16-128">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="2be16-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2be16-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="2be16-129">SYNCSTATE</span></span>](syncstate.md)

