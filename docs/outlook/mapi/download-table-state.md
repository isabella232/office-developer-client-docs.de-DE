---
title: Tabellenstatus herunterladen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5bcc8b0a-0ab7-6c3e-8334-9e83cf2882a7
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7451d159ef97ef9d8160b386ec5bf88fb388706e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338339"
---
# <a name="download-table-state"></a><span data-ttu-id="e398e-103">Tabellenstatus herunterladen</span><span class="sxs-lookup"><span data-stu-id="e398e-103">Download Table State</span></span>

  
  
<span data-ttu-id="e398e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e398e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e398e-105">In diesem Thema wird beschrieben, was während des Download-Tabellenstatus des Replikationsstatus Computers passiert.</span><span class="sxs-lookup"><span data-stu-id="e398e-105">This topic describes what happens during the download table state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e398e-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e398e-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e398e-107">Status-ID:</span><span class="sxs-lookup"><span data-stu-id="e398e-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="e398e-108">**LR_SYNC_DOWNLOAD_TABLE**</span><span class="sxs-lookup"><span data-stu-id="e398e-108">**LR_SYNC_DOWNLOAD_TABLE**</span></span> <br/> |
|<span data-ttu-id="e398e-109">Zugehörige Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="e398e-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="e398e-110">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="e398e-110">**[DNTBL](dntbl.md)**</span></span> <br/> |
|<span data-ttu-id="e398e-111">Aus folgendem Zustand:</span><span class="sxs-lookup"><span data-stu-id="e398e-111">From this state:</span></span>  <br/> |[<span data-ttu-id="e398e-112">Synchronisieren des Inhaltsstatus</span><span class="sxs-lookup"><span data-stu-id="e398e-112">Synchronize contents state</span></span>](synchronize-contents-state.md) <br/> |
|<span data-ttu-id="e398e-113">Zu folgendem Status:</span><span class="sxs-lookup"><span data-stu-id="e398e-113">To this state:</span></span>  <br/> |<span data-ttu-id="e398e-114">Synchronisieren des Inhaltsstatus</span><span class="sxs-lookup"><span data-stu-id="e398e-114">Synchronize contents state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e398e-115">Der Replikationsstatus Computer ist ein deterministischer Statuscomputer.</span><span class="sxs-lookup"><span data-stu-id="e398e-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="e398e-116">Ein Client, der von einem Staat zu einem anderen abgeht, muss schließlich aus letzterem zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="e398e-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="e398e-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e398e-117">Description</span></span>

<span data-ttu-id="e398e-118">Dieser Status initiiert das Herunterladen eines Ordners.</span><span class="sxs-lookup"><span data-stu-id="e398e-118">This state initiates downloading a folder.</span></span> <span data-ttu-id="e398e-119">Während dieses Status initialisiert Outlook die zugeordnete **DNTBL** -Datenstruktur mit Informationen über den Ordner.</span><span class="sxs-lookup"><span data-stu-id="e398e-119">During this state, Outlook initializes the associated **DNTBL** data structure with information about the folder.</span></span> <span data-ttu-id="e398e-120">Der Client downloadet den Ordnerinhalt und aktualisiert den Ordner im lokalen Speicher mit neuen Inhalten, Änderungen oder Löschungen vom Server.</span><span class="sxs-lookup"><span data-stu-id="e398e-120">The client downloads the folder contents, and updates the folder on the local store with new contents, modifications, or deletions from the server.</span></span> <span data-ttu-id="e398e-121">Der Downloadprozess übernimmt die Microsoft Exchange-inkrementelle Änderungs Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="e398e-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="e398e-122">Weitere Informationen zu ICS finden Sie unter [ICS-Auswertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e398e-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="e398e-123">Wenn dieser Status endet, gibt der lokale Speicher den Status Synchronize Content zurück.</span><span class="sxs-lookup"><span data-stu-id="e398e-123">When this state ends, the local store returns to the synchronize contents state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e398e-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e398e-124">See also</span></span>



[<span data-ttu-id="e398e-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="e398e-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e398e-126">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="e398e-126">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="e398e-127">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="e398e-127">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e398e-128">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="e398e-128">SYNCSTATE</span></span>](syncstate.md)

