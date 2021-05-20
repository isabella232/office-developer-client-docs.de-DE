---
title: Hochladen Statusstatus lesen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431540"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="2a7ea-103">Hochladen Statusstatus lesen</span><span class="sxs-lookup"><span data-stu-id="2a7ea-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="2a7ea-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a7ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="2a7ea-105">In diesem Thema wird beschrieben, was während des Statusstatus des Upload-Lesestatus des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="2a7ea-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="2a7ea-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="2a7ea-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="2a7ea-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="2a7ea-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="2a7ea-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="2a7ea-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="2a7ea-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="2a7ea-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="2a7ea-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="2a7ea-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="2a7ea-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="2a7ea-111">From this state:</span></span>  <br/> |[<span data-ttu-id="2a7ea-112">Hochladen Tabellenstatus</span><span class="sxs-lookup"><span data-stu-id="2a7ea-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="2a7ea-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="2a7ea-113">To this state:</span></span>  <br/> |<span data-ttu-id="2a7ea-114">Hochladen Tabellenstatus</span><span class="sxs-lookup"><span data-stu-id="2a7ea-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="2a7ea-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="2a7ea-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="2a7ea-116">Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="2a7ea-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="2a7ea-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a7ea-117">Description</span></span>

<span data-ttu-id="2a7ea-118">Dieser Status initiiert das Hochladen des Lesestatus von Elementen in einem Ordner, der in einem vorherigen Uploadtabelle-Status angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="2a7ea-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="2a7ea-119">Während dieses Status initialisiert Outlook die zugeordnete **UPREAD-Datenstruktur** mit Informationen zu den Elementen im Ordner, dessen Lesestatus sich geändert hat.</span><span class="sxs-lookup"><span data-stu-id="2a7ea-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="2a7ea-120">Der Client aktualisiert dann den Lesestatus dieser Elemente auf dem Server als gelesen oder ungelesen.</span><span class="sxs-lookup"><span data-stu-id="2a7ea-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="2a7ea-121">Wenn dieser Status endet, Outlook interne Informationen zum Lesestatus des Elements entfernt, was verhindert, dass der Lesestatus des Elements erneut hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="2a7ea-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="2a7ea-122">Der lokale Speicher kehrt zum Status der Uploadtabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="2a7ea-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2a7ea-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a7ea-123">See also</span></span>



[<span data-ttu-id="2a7ea-124">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="2a7ea-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="2a7ea-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="2a7ea-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="2a7ea-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="2a7ea-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="2a7ea-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="2a7ea-127">SYNCSTATE</span></span>](syncstate.md)

