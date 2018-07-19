---
title: Status „Uploadordner“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 82b00a33c5de11b3fc9ccd3bde4cf31c79b99c2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795797"
---
# <a name="upload-folder-state"></a><span data-ttu-id="bb53f-103">Status „Uploadordner“</span><span class="sxs-lookup"><span data-stu-id="bb53f-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="bb53f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bb53f-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="bb53f-105">In diesem Thema wird beschrieben, was geschieht, während der Upload Ordner Zustand des Computers Zustand Replikation.</span><span class="sxs-lookup"><span data-stu-id="bb53f-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bb53f-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="bb53f-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb53f-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="bb53f-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="bb53f-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="bb53f-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="bb53f-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="bb53f-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="bb53f-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="bb53f-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="bb53f-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="bb53f-111">From this state:</span></span>  <br/> |[<span data-ttu-id="bb53f-112">Hochladen der Hierarchie Zustand</span><span class="sxs-lookup"><span data-stu-id="bb53f-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="bb53f-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="bb53f-113">To this state:</span></span>  <br/> |<span data-ttu-id="bb53f-114">Hochladen der Hierarchie Zustand</span><span class="sxs-lookup"><span data-stu-id="bb53f-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="bb53f-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="bb53f-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="bb53f-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="bb53f-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="bb53f-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb53f-117">Description</span></span>

<span data-ttu-id="bb53f-118">Dieser Status wird initiiert, Hochladen eines Ordners in einer Hierarchie, die in einem vorherigen Upload Hierarchie Zustand angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="bb53f-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="bb53f-119">Während dieser Status wird Outlook das Folder-Objekt (sofern es nicht gelöscht) und die Kennzeichen, die den Zustand des Ordners (neue, verschoben, geändert oder gelöscht) als Teil der Datenstruktur des entsprechenden **UPFLD** .</span><span class="sxs-lookup"><span data-stu-id="bb53f-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="bb53f-120">Der Client lädt dann diese Informationen an den Server hoch.</span><span class="sxs-lookup"><span data-stu-id="bb53f-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="bb53f-121">Wenn der Hochladevorgang erfolgreich ist, wird der Client *UlFlags* in **UPFLD** auf **UPF_OK**.</span><span class="sxs-lookup"><span data-stu-id="bb53f-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="bb53f-122">Outlook löscht dann internen Informationen über die Anforderung an den Ordner hochladen.</span><span class="sxs-lookup"><span data-stu-id="bb53f-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="bb53f-123">Nach Ende der Ordner Upload gibt der lokale Speicher in den Upload Hierarchie Zustand zurück.</span><span class="sxs-lookup"><span data-stu-id="bb53f-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="bb53f-124">Basierend auf der **[UPHIER](uphier.md)** -Struktur, die auf den vorstehenden Upload Hierarchie Status entspricht, bestimmt Outlook, ob den nächsten Ordner hochladen fort und zur Vorbereitung der nächsten Upload Ordner Status.</span><span class="sxs-lookup"><span data-stu-id="bb53f-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bb53f-125">Wenn der Client nur ein Ordner hochladen muss, kann der Client die Replikation über das [Synchronisieren von Zustand](synchronize-state.md) initiieren, ohne den Upload Hierarchie Zustand.</span><span class="sxs-lookup"><span data-stu-id="bb53f-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="bb53f-126">Der Client legt bestimmte Mitglieder der **[SYNCHRONISIERUNG](sync.md)** – *UlFlags* **UPS_UPLOAD_ONLY** und **UPS_ONE_FOLDER** und *Feid* auf den Ordner ID – anzuweisen, Outlook, nur einen Ordner hochgeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="bb53f-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bb53f-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb53f-127">See also</span></span>



[<span data-ttu-id="bb53f-128">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="bb53f-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="bb53f-129">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="bb53f-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="bb53f-130">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="bb53f-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="bb53f-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="bb53f-131">SYNCSTATE</span></span>](syncstate.md)

