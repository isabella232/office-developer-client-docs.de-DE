---
title: Status des Ordners hochladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 270b1df0-c5cd-0d0f-7b57-2726dee978ab
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: c20f2998a2fef1ddb53b13708dcf56f9d7b50dbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419569"
---
# <a name="upload-folder-state"></a><span data-ttu-id="92254-103">Status des Ordners hochladen</span><span class="sxs-lookup"><span data-stu-id="92254-103">Upload Folder State</span></span>

  
  
<span data-ttu-id="92254-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="92254-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="92254-105">In diesem Thema wird beschrieben, was während des Status des Uploadordners des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="92254-105">This topic describes what happens during the upload folder state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="92254-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="92254-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92254-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="92254-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="92254-108">**LR_SYNC_UPLOAD_FOLDER**</span><span class="sxs-lookup"><span data-stu-id="92254-108">**LR_SYNC_UPLOAD_FOLDER**</span></span> <br/> |
|<span data-ttu-id="92254-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="92254-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="92254-110">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="92254-110">**[UPFLD](upfld.md)**</span></span> <br/> |
|<span data-ttu-id="92254-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="92254-111">From this state:</span></span>  <br/> |[<span data-ttu-id="92254-112">Uploadhierarchiestatus</span><span class="sxs-lookup"><span data-stu-id="92254-112">Upload hierarchy state</span></span>](upload-hierarchy-state.md) <br/> |
|<span data-ttu-id="92254-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="92254-113">To this state:</span></span>  <br/> |<span data-ttu-id="92254-114">Uploadhierarchiestatus</span><span class="sxs-lookup"><span data-stu-id="92254-114">Upload hierarchy state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="92254-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="92254-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="92254-116">Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="92254-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="92254-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92254-117">Description</span></span>

<span data-ttu-id="92254-118">Dieser Status initiiert das Hochladen eines Ordners in einer Hierarchie, die in einem vorherigen Uploadhierarchiestatus angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="92254-118">This state initiates uploading a folder in a hierarchy that has been specified in a preceding upload hierarchy state.</span></span> <span data-ttu-id="92254-119">In diesem Zustand stellt Outlook das Folder-Objekt (wenn es nicht gelöscht wurde) und die Flags, die den Status des Ordners (neu, verschoben, geändert oder gelöscht) als Teil der entsprechenden **UPFLD-Datenstruktur** angibt.</span><span class="sxs-lookup"><span data-stu-id="92254-119">During this state, Outlook provides the folder object (if it has not been deleted) and the flags indicating the state of the folder (new, moved, modified, or deleted) as part of the corresponding **UPFLD** data structure.</span></span> <span data-ttu-id="92254-120">Der Client lädt diese Informationen dann auf den Server hoch.</span><span class="sxs-lookup"><span data-stu-id="92254-120">The client then uploads this information to the server.</span></span> 
  
<span data-ttu-id="92254-121">Wenn der Upload erfolgreich war, legt der Client *ulFlags* in **UPFLD** auf **UPF_OK.**</span><span class="sxs-lookup"><span data-stu-id="92254-121">If the upload is successful, the client sets  *ulFlags*  in **UPFLD** to **UPF_OK**.</span></span> <span data-ttu-id="92254-122">Anschließend werden die internen Informationen zu der Anforderung zum Hochladen des Ordners von Outlook geräumt.</span><span class="sxs-lookup"><span data-stu-id="92254-122">Outlook then clears its internal information about the request to upload the folder.</span></span> 
  
<span data-ttu-id="92254-123">Wenn der Ordnerupload endet, kehrt der lokale Speicher zum Status der Uploadhierarchie zurück.</span><span class="sxs-lookup"><span data-stu-id="92254-123">When the folder upload ends, the local store returns to the upload hierarchy state.</span></span> <span data-ttu-id="92254-124">Basierend auf der **[UPHIER-Struktur,](uphier.md)** die dem vorherigen Uploadhierarchiestatus entspricht, bestimmt Outlook, ob mit dem Hochladen des nächsten Ordners und der Vorbereitung auf den nächsten Uploadordnerstatus fortzufahren ist.</span><span class="sxs-lookup"><span data-stu-id="92254-124">Based on the **[UPHIER](uphier.md)** structure corresponding to the preceding upload hierarchy state, Outlook determines whether to proceed with uploading the next folder and to prepare for the next upload folder state.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="92254-125">Wenn der Client nur einen Ordner hochladen muss, kann [](synchronize-state.md) der Client die Replikation über den Synchronisierungsstatus initiieren, ohne den Uploadhierarchiestatus zu betreten.</span><span class="sxs-lookup"><span data-stu-id="92254-125">If the client needs to upload only one folder, the client can initiate the replication through the [synchronize state](synchronize-state.md) without entering the upload hierarchy state.</span></span> <span data-ttu-id="92254-126">Der Client legt bestimmte Mitglieder von **[SYNC](sync.md)** fest –  *ulFlags*  auf **UPS_UPLOAD_ONLY** und **UPS_ONE_FOLDER** und  *feid*  auf die ORDNER-ID – um Outlook zu informieren, dass nur ein Ordner hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="92254-126">The client sets certain members of **[SYNC](sync.md)** —  *ulFlags*  to **UPS_UPLOAD_ONLY** and **UPS_ONE_FOLDER** and  *feid*  to the folder's ID — to tell Outlook that only one folder will be uploaded.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="92254-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92254-127">See also</span></span>



[<span data-ttu-id="92254-128">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="92254-128">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="92254-129">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="92254-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="92254-130">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="92254-130">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="92254-131">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="92254-131">SYNCSTATE</span></span>](syncstate.md)

