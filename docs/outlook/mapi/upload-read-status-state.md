---
title: Status Status des Uploads
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 4d45574e-df87-8c44-4aa7-d41b38406f0a
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e8ad2acf019df3f07060c8e8c71a62afd3fca03c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282663"
---
# <a name="upload-read-status-state"></a><span data-ttu-id="4b453-103">Status Status des Uploads</span><span class="sxs-lookup"><span data-stu-id="4b453-103">Upload Read Status State</span></span>

  
  
<span data-ttu-id="4b453-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4b453-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="4b453-105">In diesem Thema wird beschrieben, was während des Status Status des Replikats beim Hochladen des Computers geschieht.</span><span class="sxs-lookup"><span data-stu-id="4b453-105">This topic describes what happens during the upload read status state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4b453-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="4b453-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4b453-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="4b453-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="4b453-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span><span class="sxs-lookup"><span data-stu-id="4b453-108">**LR_SYNC_UPLOAD_MESSAGE_READ**</span></span> <br/> |
|<span data-ttu-id="4b453-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="4b453-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="4b453-110">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="4b453-110">**[UPREAD](upread.md)**</span></span> <br/> |
|<span data-ttu-id="4b453-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="4b453-111">From this state:</span></span>  <br/> |[<span data-ttu-id="4b453-112">Tabellenstatus hochladen</span><span class="sxs-lookup"><span data-stu-id="4b453-112">Upload table state</span></span>](upload-table-state.md) <br/> |
|<span data-ttu-id="4b453-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="4b453-113">To this state:</span></span>  <br/> |<span data-ttu-id="4b453-114">Tabellenstatus hochladen</span><span class="sxs-lookup"><span data-stu-id="4b453-114">Upload table state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="4b453-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="4b453-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="4b453-116">Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="4b453-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="4b453-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b453-117">Description</span></span>

<span data-ttu-id="4b453-118">Dieser Status initiiert das Hochladen des Lesestatus von Elementen in einem Ordner, der in einem vorherigen Upload-Tabellenstatus angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="4b453-118">This state initiates uploading the read status of items in a folder specified in a preceding upload table state.</span></span> <span data-ttu-id="4b453-119">Während dieses Status initialisiert Outlook die zugehörige **upread** -Datenstruktur mit Informationen für die Elemente im Ordner, deren Lesestatus geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="4b453-119">During this state, Outlook initializes the associated **UPREAD** data structure with information for those items in the folder whose read status has changed.</span></span> <span data-ttu-id="4b453-120">Der Client aktualisiert dann den Lesestatus dieser Elemente auf dem Server als gelesen oder ungelesen.</span><span class="sxs-lookup"><span data-stu-id="4b453-120">The client then updates the read status of these items on the server as being read or unread.</span></span> 
  
<span data-ttu-id="4b453-121">Wenn dieser Status endet, werden die internen Informationen zum Lesestatus des Elements gelöscht, und es wird verhindert, dass der Lesestatus des Elements erneut hochgeladen wird.</span><span class="sxs-lookup"><span data-stu-id="4b453-121">When this state ends, Outlook clears the internal information about the item's read status, preventing the item's read status from being uploaded again.</span></span> <span data-ttu-id="4b453-122">Der lokale Speicher gibt den Status der hochzuladenden Tabelle zurück.</span><span class="sxs-lookup"><span data-stu-id="4b453-122">The local store returns to the upload table state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="4b453-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b453-123">See also</span></span>



[<span data-ttu-id="4b453-124">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="4b453-124">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="4b453-125">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="4b453-125">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="4b453-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="4b453-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="4b453-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="4b453-127">SYNCSTATE</span></span>](syncstate.md)

