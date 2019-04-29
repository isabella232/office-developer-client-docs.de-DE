---
title: Nachrichtenstatus hochladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7fdc1494-4f40-38bd-d363-144ca70e5906
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 61cda23557a501a2651385d192f1dc7432ef1cb5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433801"
---
# <a name="upload-message-state"></a><span data-ttu-id="ae1e4-103">Nachrichtenstatus hochladen</span><span class="sxs-lookup"><span data-stu-id="ae1e4-103">Upload Message State</span></span>

  
  
<span data-ttu-id="ae1e4-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ae1e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="ae1e4-105">In diesem Thema wird beschrieben, was während des Upload-Nachrichtenstatus des Replikationsstatus Computers passiert.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-105">This topic describes what happens during the upload message state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="ae1e4-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="ae1e4-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ae1e4-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="ae1e4-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="ae1e4-108">**LR_SYNC_UPLOAD_MESSAGE**</span><span class="sxs-lookup"><span data-stu-id="ae1e4-108">**LR_SYNC_UPLOAD_MESSAGE**</span></span> <br/> |
|<span data-ttu-id="ae1e4-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="ae1e4-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="ae1e4-110">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="ae1e4-110">**[UPMSG](upmsg.md)**</span></span> <br/> |
|<span data-ttu-id="ae1e4-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="ae1e4-111">From this state:</span></span>  <br/> |[<span data-ttu-id="ae1e4-112">Tabellenstatus hochladen</span><span class="sxs-lookup"><span data-stu-id="ae1e4-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="ae1e4-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="ae1e4-113">To this state:</span></span>  <br/> |<span data-ttu-id="ae1e4-114">Tabellenstatus hochladen</span><span class="sxs-lookup"><span data-stu-id="ae1e4-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="ae1e4-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="ae1e4-116">Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="ae1e4-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae1e4-117">Description</span></span>

<span data-ttu-id="ae1e4-118">Dieser Status initiiert das Hochladen eines Outlook-Elements (e-Mail, Kalender, Kontakt, Aufgabe, Notiz oder Journal), das neu ist oder in den aktuellen Ordner verschoben wurde oder geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-118">This state initiates uploading an Outlook item (mail, calendar, contact, task, note, or journal) that is new or has been moved to the current folder, or that has been modified.</span></span> <span data-ttu-id="ae1e4-119">Outlook initialisiert die correpsonding **UPMSG** -Datenstruktur mit den entsprechenden Informationen für das Element als hinzugefügt, verschoben oder geändert.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-119">Outlook initializes the correpsonding **UPMSG** data structure with the appropriate information for the item as being added, moved, or modified.</span></span> 
  
<span data-ttu-id="ae1e4-120">Wenn das Element hinzugefügt oder verschoben wurde, wird das Element vom Client entsprechend auf dem Server hinzugefügt oder aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-120">If the item has been added or moved, the client then appropriately adds or updates the item on the server.</span></span> 
  
<span data-ttu-id="ae1e4-121">Wenn das Element geändert wurde, gibt Outlook weiter in der **UPMSG** -Datenstruktur an, ob sich die Änderungen in einem Nachrichtenkopf befinden (in diesem Fall ist das Element der Nachrichtenkopf), in den Elementeigenschaften oder im Element selbst, für das ein Konflikt erforderlich ist. Lösung.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-121">If the item has been modified, Outlook further specifies in the **UPMSG** data structure whether the modifications are in a message header (in which case the item is the message header), in the item properties, or in the item itself that requires conflict resolution.</span></span> <span data-ttu-id="ae1e4-122">Der Client aktualisiert dann das Element auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-122">The client then updates the item on the server.</span></span> 
  
<span data-ttu-id="ae1e4-123">Wenn der Upload beendet ist, stellt Outlook fest, dass die Nachricht hochgeladen wurde, sodass Sie bei einem nachfolgenden Upload nicht verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-123">When the item upload ends, Outlook notes that the message has been uploaded, so that it will not be processed in a subsequent upload.</span></span> <span data-ttu-id="ae1e4-124">Der lokale Speicher gibt den Status der hochzuladenden Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="ae1e4-124">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ae1e4-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ae1e4-125">See also</span></span>



[<span data-ttu-id="ae1e4-126">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="ae1e4-126">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="ae1e4-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ae1e4-127">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ae1e4-128">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="ae1e4-128">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="ae1e4-129">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="ae1e4-129">SYNCSTATE</span></span>](syncstate.md)

