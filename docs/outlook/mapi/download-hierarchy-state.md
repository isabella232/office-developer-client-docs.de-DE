---
title: Status „Downloadhierarchie“
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 8e0400ba-8530-e6ac-5de8-a62aeec5e10a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 45535eef75c6fc091c02ec35b669675a51e4cf48
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384857"
---
# <a name="download-hierarchy-state"></a><span data-ttu-id="e1852-103">Status „Downloadhierarchie“</span><span class="sxs-lookup"><span data-stu-id="e1852-103">Download Hierarchy State</span></span>

  
  
<span data-ttu-id="e1852-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e1852-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e1852-105">In diesem Thema wird beschrieben, während den Downloadstatus Hierarchie, von der Replikation Zustandsautomat erläutert.</span><span class="sxs-lookup"><span data-stu-id="e1852-105">This topic describes what happens during the download hierarchy state of the replication state machine.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e1852-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e1852-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e1852-107">State-ID:</span><span class="sxs-lookup"><span data-stu-id="e1852-107">State Identifier:</span></span>  <br/> |<span data-ttu-id="e1852-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span><span class="sxs-lookup"><span data-stu-id="e1852-108">**LR_SYNC_DOWNLOAD_HIERARCHY**</span></span> <br/> |
|<span data-ttu-id="e1852-109">Verwandte-Datenstruktur:</span><span class="sxs-lookup"><span data-stu-id="e1852-109">Related Data Structure:</span></span>  <br/> |<span data-ttu-id="e1852-110">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="e1852-110">**[DNHIER](dnhier.md)**</span></span> <br/> |
|<span data-ttu-id="e1852-111">Aus diesem Zustand:</span><span class="sxs-lookup"><span data-stu-id="e1852-111">From this state:</span></span>  <br/> |[<span data-ttu-id="e1852-112">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="e1852-112">Synchronize state</span></span>](synchronize-state.md) <br/> |
|<span data-ttu-id="e1852-113">Diesen Status:</span><span class="sxs-lookup"><span data-stu-id="e1852-113">To this state:</span></span>  <br/> |<span data-ttu-id="e1852-114">Synchronisieren von Zustand</span><span class="sxs-lookup"><span data-stu-id="e1852-114">Synchronize state</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="e1852-115">Das Zustandsautomat Replikation ist ein deterministisch Zustandsautomat.</span><span class="sxs-lookup"><span data-stu-id="e1852-115">The replication state machine is a deterministic state machine.</span></span> <span data-ttu-id="e1852-116">Ein Client, der von einem Zustand zu einem anderen Unternehmen muss schließlich auf die frühere letztere zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e1852-116">A client departing from one state to another must eventually return to the former from the latter.</span></span> 
  
## <a name="description"></a><span data-ttu-id="e1852-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1852-117">Description</span></span>

<span data-ttu-id="e1852-118">Dieser Status initiiert eine Strukturhierarchie von Ordnern auf einem Server auf den lokalen Speicher herunterladen.</span><span class="sxs-lookup"><span data-stu-id="e1852-118">This state initiates downloading a tree hierarchy of folders from a server to the local store.</span></span> 
  
<span data-ttu-id="e1852-119">Outlook initialisiert die zugeordnete **DNHIER** -Datenstruktur mit einem Zeiger auf der Hierarchie.</span><span class="sxs-lookup"><span data-stu-id="e1852-119">Outlook initializes the associated **DNHIER** data structure with a pointer to the hierarchy.</span></span> <span data-ttu-id="e1852-120">Der Client downloads die Hierarchie und fügt neue Ordner oder Änderungen an Ordnern im lokalen Speicher.</span><span class="sxs-lookup"><span data-stu-id="e1852-120">The client downloads the hierarchy, and inserts new folders or modifications to folders in the local store.</span></span> <span data-ttu-id="e1852-121">Der Downloadvorgang nimmt Microsoft Exchange inkrementelle Änderung Synchronisierung (ICS).</span><span class="sxs-lookup"><span data-stu-id="e1852-121">The download process adopts Microsoft Exchange Incremental Change Synchronization (ICS).</span></span> <span data-ttu-id="e1852-122">Weitere Informationen zu ICS finden Sie unter [ICS Bewertungskriterien](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e1852-122">For more information on ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span>
  
<span data-ttu-id="e1852-123">Wenn dieser Status beendet ist, gibt der lokale Speicher auf den Status synchronisieren zurück.</span><span class="sxs-lookup"><span data-stu-id="e1852-123">When this state ends, the local store returns to the synchronize state.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e1852-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e1852-124">See also</span></span>



[<span data-ttu-id="e1852-125">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="e1852-125">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e1852-126">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="e1852-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e1852-127">SYNCSTATE</span><span class="sxs-lookup"><span data-stu-id="e1852-127">SYNCSTATE</span></span>](syncstate.md)

