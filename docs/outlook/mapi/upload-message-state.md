---
title: Status „Uploadnachricht“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 430734fe98799c386e71612355b194a6b8edf00a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575413"
---
# <a name="upload-message-state"></a><span data-ttu-id="aa860-103">Status „Uploadnachricht“</span><span class="sxs-lookup"><span data-stu-id="aa860-103">Upload Message State</span></span>

  
  
<span data-ttu-id="aa860-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aa860-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="aa860-105">In diesem Thema wird beschrieben, was geschieht, während die Nachrichtenstatus Hochladen von der Replikation Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="aa860-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="aa860-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="aa860-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa860-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="aa860-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="aa860-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="aa860-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="aa860-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="aa860-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="aa860-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="aa860-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="aa860-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="aa860-111">From this state:</span></span>  <br/> |[<span data-ttu-id="aa860-112">Tabelle Zustand hochladen</span><span class="sxs-lookup"><span data-stu-id="aa860-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="aa860-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="aa860-113">To this state:</span></span>  <br/> |<span data-ttu-id="aa860-114">Tabelle Zustand hochladen</span><span class="sxs-lookup"><span data-stu-id="aa860-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="aa860-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="aa860-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="aa860-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="aa860-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="aa860-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa860-117">Description</span></span>

<span data-ttu-id="aa860-118">Dieser Status wird initiiert, Hochladen ein Outlook-Element (e-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), die neu ist oder im aktuellen Ordner verschoben wurde oder geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="aa860-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="aa860-119">Outlook initialisiert die Correpsonding **UPMSG** -Datenstruktur durch die entsprechenden Informationen für das Element wie hinzugefügt, verschoben oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="aa860-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="aa860-120">Wenn das Element hinzugefügt oder verschoben wurde, der Client dann entsprechend hinzugefügt oder das Element auf dem Server aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="aa860-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="aa860-121">Wenn das Element geändert wurde, gibt Outlook weiter in der Datenstruktur **UPMSG** , ob die Änderungen in einer e-Mail-Kopfzeile (in diesem Fall das Element der Nachrichtenkopf ist), die Elementeigenschaften oder das Element selbst, das Konflikt benötigt werden Auflösung.</span><span class="sxs-lookup"><span data-stu-id="aa860-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="aa860-122">Der Client aktualisiert anschließend das Element auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="aa860-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="aa860-123">Wenn der Hochladevorgang Element endet, Notizen Outlook, dass die Nachricht hochgeladen wurde, damit es nicht in einer nachfolgenden Upload verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="aa860-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="aa860-124">Auf den Upload Tabelle Status gibt der lokale Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="aa860-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aa860-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa860-125">See also</span></span>



[<span data-ttu-id="aa860-126">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="aa860-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="aa860-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="aa860-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="aa860-128">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="aa860-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="aa860-129">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="aa860-129">SYNCSTATE</span></span>](syncstate.md)

