---
title: Synchronisieren von Zustand
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270ff414-514c-b1fc-db48-761bf6de8867
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 36bdeecfaaa94492b1e719dbd1cf455bfa40db47
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795698"
---
# <a name="synchronize-state"></a><span data-ttu-id="691fc-103">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="691fc-103">Synchronize State</span></span>

  
  
<span data-ttu-id="691fc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="691fc-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="691fc-105">In diesem Thema wird beschrieben, was geschieht, während die Synchronize-Zustand des Computers Zustand Replikation.</span><span class="sxs-lookup"><span data-stu-id="691fc-105">This topic describes what happens during the synchronize state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="691fc-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="691fc-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="691fc-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="691fc-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="691fc-108">**LR_SYNC**</span><span class="sxs-lookup"><span data-stu-id="691fc-108">**LR_SYNC**</span></span> <br/> |
|<span data-ttu-id="691fc-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="691fc-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="691fc-110">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="691fc-110">**[SYNC](sync.md)**</span></span> <br/> |
|<span data-ttu-id="691fc-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="691fc-111">From this state:</span></span>  <br/> |[<span data-ttu-id="691fc-112">Leerlauf</span><span class="sxs-lookup"><span data-stu-id="691fc-112">Idle state</span></span>](idle-state.md) <br/> |
|<span data-ttu-id="691fc-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="691fc-113">To this state:</span></span>  <br/> |<span data-ttu-id="691fc-114">[Hierarchie Downloadstatus](download-hierarchy-state.md), [Synchronisieren Inhalt Zustand](synchronize-contents-state.md), [Hierarchie Zustand hochladen](upload-hierarchy-state.md)oder Leerlauf</span><span class="sxs-lookup"><span data-stu-id="691fc-114">[Download hierarchy state](download-hierarchy-state.md), [synchronize contents state](synchronize-contents-state.md), [upload hierarchy state](upload-hierarchy-state.md), or idle state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="691fc-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="691fc-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="691fc-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="691fc-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="691fc-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="691fc-117">Description</span></span>

<span data-ttu-id="691fc-118">Dieser Status wird die Synchronisierung initiiert.</span><span class="sxs-lookup"><span data-stu-id="691fc-118">This state initiates synchronization.</span></span> <span data-ttu-id="691fc-119">Ein lokales Speichers Übergang kann ein Upload oder eine Downloadstatus von hier aus.</span><span class="sxs-lookup"><span data-stu-id="691fc-119">A local store can transition to an upload or a download state from here.</span></span> <span data-ttu-id="691fc-120">Beispielsweise ein lokales Speichers kann auf den Upload Hierarchie Status zu eine Ordnerhierarchie auf den Server hochzuladen verschieben oder sie können eine vollständige Synchronisierung durchführen, indem ersten Hochladen der Hierarchie und klicken Sie dann die Hierarchie vom Server herunterladen.</span><span class="sxs-lookup"><span data-stu-id="691fc-120">For example, a local store can move to the upload hierarchy state to upload a folder hierarchy to the server, or it can perform a full synchronization by first uploading the hierarchy and then downloading the hierarchy from the server.</span></span>
  
<span data-ttu-id="691fc-121">Während dieser Zustand initialisiert Outlook die zugeordnete **SYNC** -Datenstruktur durch den Pfad zu dem lokalen Speicher, damit Outlook Änderungen bei der anderen Status sieht.</span><span class="sxs-lookup"><span data-stu-id="691fc-121">During this state, Outlook initializes the associated **SYNC** data structure with the path to the local store, so that Outlook sees modifications during other states.</span></span> 
  
<span data-ttu-id="691fc-122">Der Client legt die [in] Mitglieder der **SYNCHRONISIERUNG**, die Outlook mitteilt, wie anderen Zustände behandelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="691fc-122">The client sets the [in] members of **SYNC**, which tells Outlook how to handle other states.</span></span> <span data-ttu-id="691fc-123">Beispielsweise kann der Client *UlFlags* auf **UPS_UPLOAD_ONLY** und **UPS_THESE_FOLDERS** festgelegt und *Pel* und eine Liste der Ordner an, Outlook, dass nur diese Ordner Eintragsbezeichner wird hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="691fc-123">For example, the client can set  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_THESE_FOLDERS** and  *pel*  to a list of entry identifiers of the folders to tell Outlook that only these folders will be uploaded.</span></span> <span data-ttu-id="691fc-124">Wenn dieser Status beendet wird, wird der lokale Speicher in den Leerlauf zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="691fc-124">When this state ends, the local store reverts to the idle state.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="691fc-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="691fc-125">See also</span></span>



[<span data-ttu-id="691fc-126">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="691fc-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="691fc-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="691fc-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="691fc-128">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="691fc-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="691fc-129">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="691fc-129">SYNCSTATE</span></span>](syncstate.md)

