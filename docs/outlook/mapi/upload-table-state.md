---
title: Tabellenstatus hochladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342840"
---
# <a name="upload-table-state"></a><span data-ttu-id="33b5e-103">Tabellenstatus hochladen</span><span class="sxs-lookup"><span data-stu-id="33b5e-103">Upload Table State</span></span>

  
  
<span data-ttu-id="33b5e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="33b5e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="33b5e-105">In diesem Thema wird beschrieben, was während des Upload-Tabellenstatus des Replikationsstatus Computers passiert.</span><span class="sxs-lookup"><span data-stu-id="33b5e-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="33b5e-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="33b5e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="33b5e-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="33b5e-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="33b5e-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="33b5e-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="33b5e-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="33b5e-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="33b5e-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="33b5e-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="33b5e-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="33b5e-111">From this state:</span></span>  <br/> |[<span data-ttu-id="33b5e-112">Synchronisieren des Inhaltsstatus</span><span class="sxs-lookup"><span data-stu-id="33b5e-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="33b5e-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="33b5e-113">To this state:</span></span>  <br/> |<span data-ttu-id="33b5e-114">[Nachrichtenstatus hochladen](upload-message-state.md), [Löschstatus](upload-delete-status-state.md)hochladen, Status [Lesen hochladen](upload-read-status-state.md)oder Inhaltsstatus synchronisieren</span><span class="sxs-lookup"><span data-stu-id="33b5e-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="33b5e-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="33b5e-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="33b5e-116">Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="33b5e-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="33b5e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="33b5e-117">Description</span></span>

<span data-ttu-id="33b5e-118">Dieser Status initiiert das Hochladen des Inhalts eines Ordners, der in einem vorhergehenden Synchronisierungsstatus angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="33b5e-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="33b5e-119">Der Ordner kann ein Mail-, Kalender-, Kontakt-, Aufgaben-, Notizen-oder Journalordner sein.</span><span class="sxs-lookup"><span data-stu-id="33b5e-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="33b5e-120">Während dieses Zustands erstellt Outlook eine Liste von Elementen, die hinzugefügt, geändert, verschoben, gelöscht oder als gelesen markiert wurden, und bereitet die entsprechenden internen Informationen für den entsprechenden Upload-Status, den Zustand "Delete" oder "Lesestatus hochladen" vor. Staat.</span><span class="sxs-lookup"><span data-stu-id="33b5e-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="33b5e-121">Wenn dieser Status endet, markiert Outlook den Ordner als den Inhalt synchronisiert, sodass der Inhalt nicht erneut hochgeladen werden, bis eine andere Änderung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="33b5e-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="33b5e-122">Der lokale Speicher gibt den Status "Inhalte synchronisieren" zurück.</span><span class="sxs-lookup"><span data-stu-id="33b5e-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="33b5e-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="33b5e-123">See also</span></span>



[<span data-ttu-id="33b5e-124">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="33b5e-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="33b5e-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="33b5e-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="33b5e-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="33b5e-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="33b5e-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="33b5e-127">SYNCSTATE</span></span>](syncstate.md)

