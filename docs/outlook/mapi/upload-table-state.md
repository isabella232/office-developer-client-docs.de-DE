---
title: Hochladen Tabellenstatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a2a9b3f214c76b8ec965c84c4731e0dc57e83352
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405821"
---
# <a name="upload-table-state"></a><span data-ttu-id="8092c-103">Hochladen Tabellenstatus</span><span class="sxs-lookup"><span data-stu-id="8092c-103">Upload Table State</span></span>

  
  
<span data-ttu-id="8092c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8092c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8092c-105">In diesem Thema wird beschrieben, was während des Status der Uploadtabelle des Replikationsstatuscomputers geschieht.</span><span class="sxs-lookup"><span data-stu-id="8092c-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="8092c-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="8092c-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8092c-107">Statusbezeichner:</span><span class="sxs-lookup"><span data-stu-id="8092c-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="8092c-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="8092c-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="8092c-109">Verwandte Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="8092c-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="8092c-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="8092c-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="8092c-111">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="8092c-111">From this state:</span></span>  <br/> |[<span data-ttu-id="8092c-112">Synchronisieren des Inhaltszustands</span><span class="sxs-lookup"><span data-stu-id="8092c-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="8092c-113">In diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="8092c-113">To this state:</span></span>  <br/> |<span data-ttu-id="8092c-114">[Hochladen Status der Nachricht,](upload-message-state.md) [Statusstatus zum](upload-delete-status-state.md)Hochladen des Löschstatus, [Statusstatus](upload-read-status-state.md)des Leseinhalts hochladen oder Inhaltsstatus synchronisieren</span><span class="sxs-lookup"><span data-stu-id="8092c-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="8092c-115">Der Replikationsstatuscomputer ist ein deterministischer Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="8092c-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="8092c-116">Ein Client, der von einem Zustand in einen anderen abt, muss schließlich zu dem ersten von letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="8092c-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="8092c-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8092c-117">Description</span></span>

<span data-ttu-id="8092c-118">Dieser Zustand initiiert das Hochladen des Inhalts eines Ordners, der in einem vorherigen Synchronisierungsinhaltsstatus angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8092c-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="8092c-119">Der Ordner kann ein E-Mail-, Kalender-, Kontakt-, Aufgaben-, Notizen- oder Journalordner sein.</span><span class="sxs-lookup"><span data-stu-id="8092c-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="8092c-120">Während dieses Status erstellt Outlook eine Liste der Elemente, die hinzugefügt, geändert, verschoben, gelöscht oder als gelesen markiert wurden, und bereitet die entsprechenden internen Informationen für den entsprechenden Status der Uploadnachricht, den Status "Löschstatus hochladen" oder "Lesestatus hochladen" vor.</span><span class="sxs-lookup"><span data-stu-id="8092c-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="8092c-121">Wenn dieser Status endet, Outlook der Ordner als synchronisiert markiert, sodass der Inhalt erst wieder hochgeladen wird, wenn eine weitere Änderung vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="8092c-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="8092c-122">Der lokale Speicher kehrt zum Status "Inhalt synchronisieren" zurück.</span><span class="sxs-lookup"><span data-stu-id="8092c-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8092c-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8092c-123">See also</span></span>



[<span data-ttu-id="8092c-124">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="8092c-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="8092c-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="8092c-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="8092c-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="8092c-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="8092c-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="8092c-127">SYNCSTATE</span></span>](syncstate.md)

