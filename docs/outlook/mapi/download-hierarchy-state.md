---
title: Status „Downloadhierarchie“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9c334bc86bdff4abb2762642a37e3f0933a0b29
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589028"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="aec55-103">Status „Downloadhierarchie“</span><span class="sxs-lookup"><span data-stu-id="aec55-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="aec55-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="aec55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="aec55-105">In diesem Thema wird beschrieben, während den Downloadstatus Hierarchie, von der Replikation Zustandsautomat erläutert.</span><span class="sxs-lookup"><span data-stu-id="aec55-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="aec55-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="aec55-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aec55-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="aec55-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="aec55-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="aec55-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="aec55-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="aec55-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="aec55-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="aec55-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="aec55-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="aec55-111">From this state:</span></span>  <br/> |[<span data-ttu-id="aec55-112">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="aec55-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="aec55-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="aec55-113">To this state:</span></span>  <br/> |<span data-ttu-id="aec55-114">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="aec55-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="aec55-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="aec55-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="aec55-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="aec55-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="aec55-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aec55-117">Description</span></span>

<span data-ttu-id="aec55-118">Dieser Status initiiert eine Strukturhierarchie von Ordnern auf einem Server auf den lokalen Speicher herunterladen.</span><span class="sxs-lookup"><span data-stu-id="aec55-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="aec55-119">Outlook initialisiert die zugeordnete **DNHIER** -Datenstruktur mit einem Zeiger auf der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="aec55-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="aec55-120">Der Client downloads die Hierarchie und fügt neue Ordner oder Änderungen an Ordnern im lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="aec55-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="aec55-121">Der Downloadvorgang nimmt Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="aec55-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="aec55-122">Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="aec55-122">For more information on ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="aec55-123">Wenn dieser Status beendet ist, gibt der lokale Speicher auf den Status synchronisieren zurück.</span><span class="sxs-lookup"><span data-stu-id="aec55-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aec55-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aec55-124">See also</span></span>



[<span data-ttu-id="aec55-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="aec55-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="aec55-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="aec55-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="aec55-127">SYNCHRONISIERUNGSSTATUS</span><span class="sxs-lookup"><span data-stu-id="aec55-127">SYNCSTATE</span></span>](syncstate.md)

