---
title: Status „Status des Upload-Lesevorgangs“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 41815a88fe1215d2a85a38592e04b0d0bbd43cc6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573047"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="4ef83-103">Status „Status des Upload-Lesevorgangs“</span><span class="sxs-lookup"><span data-stu-id="4ef83-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="4ef83-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4ef83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4ef83-105">In diesem Thema wird beschrieben, was geschieht, während der Upload Status Zustand des Computers Zustand Replikation lesen.</span><span class="sxs-lookup"><span data-stu-id="4ef83-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4ef83-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4ef83-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ef83-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="4ef83-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4ef83-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="4ef83-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="4ef83-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="4ef83-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4ef83-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="4ef83-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="4ef83-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="4ef83-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4ef83-112">Tabelle Zustand hochladen</span><span class="sxs-lookup"><span data-stu-id="4ef83-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="4ef83-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="4ef83-113">To this state:</span></span>  <br/> |<span data-ttu-id="4ef83-114">Tabelle Zustand hochladen</span><span class="sxs-lookup"><span data-stu-id="4ef83-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4ef83-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="4ef83-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4ef83-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="4ef83-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4ef83-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4ef83-117">Description</span></span>

<span data-ttu-id="4ef83-118">Dieser Status wird initiiert, Hochladen des Status Lesen von Elementen in einem Ordner, in den vorstehenden Upload-Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="4ef83-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="4ef83-119">Während dieser Zustand initialisiert Outlook die zugeordnete **UPREAD** -Datenstruktur mit Informationen für diese Elemente im Ordner, deren Status Lesen geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4ef83-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="4ef83-120">Der Client aktualisiert anschließend den lesen Status dieser Elemente auf dem Server als gelesen oder ungelesen.</span><span class="sxs-lookup"><span data-stu-id="4ef83-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="4ef83-121">Wenn dieser Status beendet ist, löscht Outlook die interne Informationen über das Element gelesen-Status, verhindert, dass das Element gelesen-Status wird erneut hochgeladen.</span><span class="sxs-lookup"><span data-stu-id="4ef83-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="4ef83-122">Auf den Upload Tabelle Status gibt der lokale Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="4ef83-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4ef83-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ef83-123">See also</span></span>



[<span data-ttu-id="4ef83-124">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="4ef83-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4ef83-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4ef83-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4ef83-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="4ef83-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4ef83-127">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="4ef83-127">SYNCSTATE</span></span>](syncstate.md)

