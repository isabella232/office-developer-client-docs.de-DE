---
title: Status „Uploadtabelle“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: fe167c90-c817-b627-0728-5c6393477c22
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 454df4dde2062d20855e4d9bceaf4400669693ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795808"
---
# <a name="upload-table-state"></a><span data-ttu-id="30ead-103">Status „Uploadtabelle“</span><span class="sxs-lookup"><span data-stu-id="30ead-103">Upload Table State</span></span>

  
  
<span data-ttu-id="30ead-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="30ead-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="30ead-105">In diesem Thema wird beschrieben, was geschieht, während die Tabelle Zustand der Replikation Zustandsautomat hochladen.</span><span class="sxs-lookup"><span data-stu-id="30ead-105">This topic describes what happens during the upload table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="30ead-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="30ead-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="30ead-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="30ead-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="30ead-108">**LR_SYNC_UPLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="30ead-108">**LR_SYNC_UPLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="30ead-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="30ead-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="30ead-110">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="30ead-110">**[UPTBL](uptbl.md)**</span></span> <br/> |
|<span data-ttu-id="30ead-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="30ead-111">From this state:</span></span>  <br/> |[<span data-ttu-id="30ead-112">Synchronisieren von Inhalt Zustand</span><span class="sxs-lookup"><span data-stu-id="30ead-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="30ead-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="30ead-113">To this state:</span></span>  <br/> |<span data-ttu-id="30ead-114">[Nachrichtenstatus hochladen](upload-message-state.md), [Upload löschen Status Zustand](upload-delete-status-state.md), [Status Zustand lesen hochladen](upload-read-status-state.md), oder Inhalt Zustand synchronisieren</span><span class="sxs-lookup"><span data-stu-id="30ead-114">[Upload message state](upload-message-state.md), [upload delete status state](upload-delete-status-state.md), [upload read status state](upload-read-status-state.md), or synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="30ead-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="30ead-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="30ead-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="30ead-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="30ead-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30ead-117">Description</span></span>

<span data-ttu-id="30ead-118">Dieser Status wird initiiert, Hochladen den Inhalt eines Ordners, der in einem vorherigen synchronisieren Inhalt Zustand angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="30ead-118">This state initiates uploading the contents of a folder that has been specified in a preceding synchronize contents state.</span></span> <span data-ttu-id="30ead-119">Der Ordner kann einen Ordner e-Mail, Kalender, Kontakte, Aufgaben, Notizen oder Journal sein.</span><span class="sxs-lookup"><span data-stu-id="30ead-119">The folder can be a mail, calendar, contacts, tasks, notes, or journal folder.</span></span> <span data-ttu-id="30ead-120">Während dieser Zustand Outlook erstellt eine Liste der Elemente, die hinzugefügt, geändert, verschoben, gelöscht, oder wurden als gelesen markiert und bereitet die entsprechende interne Informationen für den entsprechenden Upload Nachrichtenstatus, Upload löschen Status Zustand oder Status "gelesen" Hochladen Zustand.</span><span class="sxs-lookup"><span data-stu-id="30ead-120">During this state, Outlook creates a list of items that have been added, modified, moved, deleted, or marked as read, and prepares the appropriate internal information for the corresponding upload message state, upload delete status state, or upload read status state.</span></span>
  
<span data-ttu-id="30ead-121">Wenn dieser Status beendet wird, markiert Outlook den Ordner mit seinen Inhalt synchronisiert, sodass der Inhalt nicht erneut hochgeladen werden soll, bis eine andere Änderung vorgenommen wird.</span><span class="sxs-lookup"><span data-stu-id="30ead-121">When this state ends, Outlook marks the folder as having its contents synchronized, so that the contents will not be uploaded again until another modification is made.</span></span> <span data-ttu-id="30ead-122">Auf den Synchronize Inhalt Status gibt der lokale Speicher zurück.</span><span class="sxs-lookup"><span data-stu-id="30ead-122">The local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="30ead-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30ead-123">See also</span></span>



[<span data-ttu-id="30ead-124">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="30ead-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="30ead-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="30ead-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="30ead-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="30ead-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="30ead-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="30ead-127">SYNCSTATE</span></span>](syncstate.md)

