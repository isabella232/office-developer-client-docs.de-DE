---
title: Ordner Status hochladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348426"
---
# <a name="upload-folder-state"></a><span data-ttu-id="a881b-103">Ordner Status hochladen</span><span class="sxs-lookup"><span data-stu-id="a881b-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="a881b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a881b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="a881b-105">In diesem Thema wird beschrieben, was während des Upload-Ordner Status des Replikationsstatus Computers passiert.</span><span class="sxs-lookup"><span data-stu-id="a881b-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="a881b-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a881b-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a881b-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="a881b-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="a881b-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="a881b-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="a881b-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="a881b-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="a881b-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="a881b-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="a881b-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="a881b-111">From this state:</span></span>  <br/> |[<span data-ttu-id="a881b-112">Hierarchie Status hochladen</span><span class="sxs-lookup"><span data-stu-id="a881b-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="a881b-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="a881b-113">To this state:</span></span>  <br/> |<span data-ttu-id="a881b-114">Hierarchie Status hochladen</span><span class="sxs-lookup"><span data-stu-id="a881b-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="a881b-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="a881b-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="a881b-116">Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="a881b-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="a881b-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a881b-117">Description</span></span>

<span data-ttu-id="a881b-118">Dieser Status initiiert das Hochladen eines Ordners in einer Hierarchie, der in einem vorangehenden Upload-Hierarchie Status angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a881b-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="a881b-119">In diesem Zustand stellt Outlook das Folder-Objekt (falls es nicht gelöscht wurde) und die Flags bereit, die den Status des Ordners (neu, verschoben, geändert oder gelöscht) als Teil der entsprechenden **UPFLD** -Datenstruktur angeben.</span><span class="sxs-lookup"><span data-stu-id="a881b-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="a881b-120">Der Client lädt diese Informationen dann auf den Server hoch.</span><span class="sxs-lookup"><span data-stu-id="a881b-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="a881b-121">Wenn der Upload erfolgreich ist, legt der Client *ulFlags* in **UPFLD** auf **UPF_OK**fest.</span><span class="sxs-lookup"><span data-stu-id="a881b-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="a881b-122">Outlook löscht dann die internen Informationen zu der Anforderung, den Ordner hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="a881b-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="a881b-123">Wenn der Ordner Upload beendet wird, wird der lokale Speicher zum Upload-Hierarchie Status zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a881b-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="a881b-124">Basierend auf der **[uphier](uphier.md)** -Struktur, die dem vorangehenden Upload-Hierarchie Status entspricht, bestimmt Outlook, ob das Hochladen des nächsten Ordners fortgesetzt und der nächste Upload-Ordner Status vorbereitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a881b-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a881b-125">Wenn der Client nur einen Ordner hochladen muss, kann der Client die Replikation über den [Status Synchronize](synchronize-state.md) initiieren, ohne den Upload-Hierarchie Status einzugeben.</span><span class="sxs-lookup"><span data-stu-id="a881b-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="a881b-126">Der Client legt bestimmte Synchronisierungs **[](sync.md)** Mitglieder – *ulFlags* auf **UPS_UPLOAD_ONLY** und **UPS_ONE_FOLDER** und *Feid* auf die ID des Ordners – fest, um Outlook mitzuteilen, dass nur ein Ordner hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="a881b-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a881b-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a881b-127">See also</span></span>



[<span data-ttu-id="a881b-128">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="a881b-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="a881b-129">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a881b-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="a881b-130">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="a881b-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="a881b-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="a881b-131">SYNCSTATE</span></span>](syncstate.md)

